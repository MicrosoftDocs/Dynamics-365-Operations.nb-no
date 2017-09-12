---
title: Kontantrabatt
description: "Kontantrabatter konfigureres og deles for leverandører og kunder.  Den tilgjengelige kontantrabatten kan defineres på kundefaktura eller leverandørfaktura, og brukes hvis fakturaen betales innen kontantrabattdatoen."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 668e3ebdd2729efb48e2833fd5beec3cefdb17b0
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---

# <a name="cash-discounts"></a><span data-ttu-id="1436f-104">Kontantrabatt</span><span class="sxs-lookup"><span data-stu-id="1436f-104">Cash discounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1436f-105">Kontantrabatter konfigureres og deles for leverandører og kunder.</span><span class="sxs-lookup"><span data-stu-id="1436f-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="1436f-106">Den tilgjengelige kontantrabatten kan defineres på kundefaktura eller leverandørfaktura, og brukes hvis fakturaen betales innen kontantrabattdatoen.</span><span class="sxs-lookup"><span data-stu-id="1436f-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

<a name="cash-discounts"></a><span data-ttu-id="1436f-107">Kontantrabatt</span><span class="sxs-lookup"><span data-stu-id="1436f-107">Cash discounts</span></span>
--------------

<span data-ttu-id="1436f-108">Kontantrabatter for både kunder eller leverandører kan opprettes på siden for kontantrabatter.</span><span class="sxs-lookup"><span data-stu-id="1436f-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="1436f-109">Du kan også definere, ved hjelp av feltet Neste rabattkode, en serie med kontantrabatter som kommer etter hverandre etter hvert som tidligere kontantrabattdatoer utløper.</span><span class="sxs-lookup"><span data-stu-id="1436f-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="1436f-110">Hvis du vil ha mer informasjon, se "Eksempel: Serie med kontantrabatter" senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="1436f-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="1436f-111">Hvis fakturaen, kredittransaksjonen (en betaling eller en kreditnota) eller begge deler er angitt i en annen valuta enn regnskapsvalutaen for den juridiske enheten, blir kontantrabatten beregnet ved hjelp av valutakursen som er basert på datoen for betalingen eller kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="1436f-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="1436f-112">Hvis fakturaen eller kredittdokumentet er angitt i ulike juridiske enheter, og hvis regnskapsvalutaene for de juridiske enhetene er forskjellige, hentes valutakursen fra den juridiske enheten for fakturaen, i henhold til datoen for kredittdokumentet.</span><span class="sxs-lookup"><span data-stu-id="1436f-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="1436f-113">Hvis du vil ha mer informasjon, se "Eksempel: Valutakurser for kontantrabatter" senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="1436f-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>
<span data-ttu-id="1436f-114">Standardrekkefølge for kontantrabatthovedkonto</span><span class="sxs-lookup"><span data-stu-id="1436f-114">Defaulting order of cash discount main account</span></span>
----------------------------------------------

<span data-ttu-id="1436f-115">Hvis en faktura betales tidsnok til å få en kontantrabatt, posteres kontantrabatten automatisk til en kontantrabatthovedkonto i henhold til følgende standardprioritet:</span><span class="sxs-lookup"><span data-stu-id="1436f-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="1436f-116">Hovedkontoen som er angitt i feltet Alternativ kontantrabattkonto på kundesiden Utlign åpne transaksjoner eller leverandørsiden Utlign åpne transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="1436f-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="1436f-117">Hovedkontoen som er angitt i feltet Kundekontantrabatt eller i feltet Leverandørkontantrabatt for finansposteringsgruppen som er tilordnet mva-koden for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1436f-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="1436f-118">Definer finansposteringsgrupper på siden Finansposteringsgrupper, og tilordne dem til mva-koder på siden for mva-koder.</span><span class="sxs-lookup"><span data-stu-id="1436f-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="1436f-119">Den primære posteringskontoen på siden Kontantrabatter i feltet Hovedkonto for kunderabatter eller feltet Hovedkonto for leverandørrabatter for kontantrabattkoden som finnes på den utlignede fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1436f-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="1436f-120">Hovedkontoen for kontantrabatter, som definert på siden Kontoer for automatiske transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="1436f-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="1436f-121">Eksempel: Serie med kontantrabatter</span><span class="sxs-lookup"><span data-stu-id="1436f-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="1436f-122">Definer tre kontantrabattkoder på denne måten:</span><span class="sxs-lookup"><span data-stu-id="1436f-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="1436f-123">Kode 5D10% – En kontantrabatt på 10 % hvis beløpet betales innen 5 dager.</span><span class="sxs-lookup"><span data-stu-id="1436f-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="1436f-124">Kode 10D5% – En kontantrabatt på 5 % hvis beløpet betales innen 10 dager.</span><span class="sxs-lookup"><span data-stu-id="1436f-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="1436f-125">Kode 14D2% – En kontantrabatt på 2 % hvis beløpet betales innen 14 dager.</span><span class="sxs-lookup"><span data-stu-id="1436f-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="1436f-126">I feltet Neste rabattkode:</span><span class="sxs-lookup"><span data-stu-id="1436f-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="1436f-127">For 5D10%-koden velger du 10D5%.</span><span class="sxs-lookup"><span data-stu-id="1436f-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="1436f-128">For 10D5%-koden velger du 14D2%.</span><span class="sxs-lookup"><span data-stu-id="1436f-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="1436f-129">For 14D2%-koden lar du feltet Neste rabattkode stå tomt.</span><span class="sxs-lookup"><span data-stu-id="1436f-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="1436f-130">De tre kontantrabattene følger hverandre når betalingsdatoen overskrider den forrige kontantrabattdatoen på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1436f-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="1436f-131">Bare én kontantrabatt gis når fakturaen er betalt, basert på hvilken kontantrabattdato som oppfylles i sekvensen med kontantrabatter.</span><span class="sxs-lookup"><span data-stu-id="1436f-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="1436f-132">Eksempel: Valutakurser for kontantrabatter</span><span class="sxs-lookup"><span data-stu-id="1436f-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="1436f-133">Regnskapsvalutaen for den juridiske enheten er EUR, og følgende valutakurser er angitt for USD:</span><span class="sxs-lookup"><span data-stu-id="1436f-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="1436f-134">1. februar = 110</span><span class="sxs-lookup"><span data-stu-id="1436f-134">February 1 = 110</span></span>
-   <span data-ttu-id="1436f-135">1. mars = 80</span><span class="sxs-lookup"><span data-stu-id="1436f-135">March 1 = 80</span></span>

<span data-ttu-id="1436f-136">Det posteres en faktura på USD 1 000 med vilkårene for kontantrabatt på 20D2% 15. februar.</span><span class="sxs-lookup"><span data-stu-id="1436f-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="1436f-137">Regnskapsvalutabeløpet på fakturaen er 1100 EUR.</span><span class="sxs-lookup"><span data-stu-id="1436f-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="1436f-138">En betaling på USD 980 betales med fakturaen 1. mars.</span><span class="sxs-lookup"><span data-stu-id="1436f-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="1436f-139">Kontantrabattbeløpet er USD 20.</span><span class="sxs-lookup"><span data-stu-id="1436f-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="1436f-140">Regnskapsvalutabeløpet for betalingen er EUR 784.</span><span class="sxs-lookup"><span data-stu-id="1436f-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="1436f-141">Regnskapsvalutabeløpet for kontantrabatten blir beregnet ved hjelp av valutakursen 1. mars: 20 \* 80 / 100 = EUR 16.</span><span class="sxs-lookup"><span data-stu-id="1436f-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>
| <span data-ttu-id="1436f-142">**Obs!**</span><span class="sxs-lookup"><span data-stu-id="1436f-142">**Note**</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1436f-143">Hvis alternativet Beregn kontantrabatter for delvise betalinger velges på siden Kundeparametere eller Leverandørparametere, brukes valutakursen som er i kraft på datoen for hver delbetaling.</span><span class="sxs-lookup"><span data-stu-id="1436f-143">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> |

 
=

 




