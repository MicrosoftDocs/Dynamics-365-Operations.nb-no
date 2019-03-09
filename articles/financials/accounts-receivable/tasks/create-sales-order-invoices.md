---
title: Opprette salgsordrefakturaer
description: Denne oppgaveveiledningen beskriver fakturering av salgsordren, inkludert fletting av fakturaer og satsvis behandling.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a57d204c0dcb44cbce7a0cc4d2f00b75b57e219
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "353316"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="31e6d-103">Opprette salgsordrefakturaer</span><span class="sxs-lookup"><span data-stu-id="31e6d-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31e6d-104">Denne oppgaveveiledningen beskriver fakturering av salgsordren, inkludert fletting av fakturaer og satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="31e6d-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="31e6d-105">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="31e6d-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="31e6d-106">Opprette en faktura fra en salgsordre</span><span class="sxs-lookup"><span data-stu-id="31e6d-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="31e6d-107">Gå til Kunder > Ordrer > Salgsordrer som er sendt, men ikke fakturert.</span><span class="sxs-lookup"><span data-stu-id="31e6d-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="31e6d-108">Velg en salgsordre fra listen.</span><span class="sxs-lookup"><span data-stu-id="31e6d-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="31e6d-109">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="31e6d-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="31e6d-110">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="31e6d-110">Click Invoice.</span></span>
    * <span data-ttu-id="31e6d-111">Legg merke til at denne salgsordren har flere følgesedler tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="31e6d-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="31e6d-112">Den viser bare ordet <multiple> i stedet for følgeseddelnummeret.</span><span class="sxs-lookup"><span data-stu-id="31e6d-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="31e6d-113">Utvid seksjonen Parametere.</span><span class="sxs-lookup"><span data-stu-id="31e6d-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="31e6d-114">Postering må settes til Ja for å postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="31e6d-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="31e6d-115">Du kan også slå av postering, og du kan bare skrive ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="31e6d-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="31e6d-116">Du kan imidlertid oppnå samme resultat ved å opprette en proformafaktura i stedet for en faktura.</span><span class="sxs-lookup"><span data-stu-id="31e6d-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="31e6d-117">Dette alternativet brukes for satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="31e6d-117">This option is used for batch jobs.</span></span> <span data-ttu-id="31e6d-118">Spørringen kjøres når den satsvise jobben kjøres.</span><span class="sxs-lookup"><span data-stu-id="31e6d-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="31e6d-119">Velg Etter i feltet Skriv ut.</span><span class="sxs-lookup"><span data-stu-id="31e6d-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="31e6d-120">Velg Ja for å skrive ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="31e6d-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="31e6d-121">Utskriftsbehandling kan skrive ut flere eksemplarer av fakturaen, og også sende fakturaen via e-post som en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="31e6d-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="31e6d-122">Velg Summer i feltet Skriv ut tillegg.</span><span class="sxs-lookup"><span data-stu-id="31e6d-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="31e6d-123">I feltet Kontroller kredittgrense velger du Saldo.</span><span class="sxs-lookup"><span data-stu-id="31e6d-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="31e6d-124">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="31e6d-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="31e6d-125">Kombinere ordrer til én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="31e6d-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="31e6d-126">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="31e6d-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="31e6d-127">Finn en kunde som har flere fakturaer som er åpne.</span><span class="sxs-lookup"><span data-stu-id="31e6d-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="31e6d-128">Velg en åpen salgsordre.</span><span class="sxs-lookup"><span data-stu-id="31e6d-128">Select an open sales order.</span></span>
4. <span data-ttu-id="31e6d-129">Velg en ny åpen salgsordre for den samme kunden.</span><span class="sxs-lookup"><span data-stu-id="31e6d-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="31e6d-130">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="31e6d-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="31e6d-131">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="31e6d-131">Click Invoice.</span></span>
7. <span data-ttu-id="31e6d-132">Utvid seksjonen Parametere.</span><span class="sxs-lookup"><span data-stu-id="31e6d-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="31e6d-133">Velg Alle i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="31e6d-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="31e6d-134">Legg merke til at det finnes to fakturaer som er oppført i oversiktsdelen.</span><span class="sxs-lookup"><span data-stu-id="31e6d-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="31e6d-135">Nå skal vi slå dem sammen til én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="31e6d-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="31e6d-136">I samleoppdateringen for feltet velger du "Fakturakonto".</span><span class="sxs-lookup"><span data-stu-id="31e6d-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="31e6d-137">Klikk Ordre for å slå sammen salgsordrene til én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="31e6d-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="31e6d-138">De to ordrene er nå slått sammen til én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="31e6d-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="31e6d-139">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="31e6d-139">Click Cancel.</span></span>
12. <span data-ttu-id="31e6d-140">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="31e6d-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="31e6d-141">Postere fakturaer i en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="31e6d-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="31e6d-142">Gå til Kunder > Fakturaer > Partifakturering > Faktura.</span><span class="sxs-lookup"><span data-stu-id="31e6d-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="31e6d-143">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="31e6d-143">Click Select.</span></span>
3. <span data-ttu-id="31e6d-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="31e6d-144">Click OK.</span></span>
4. <span data-ttu-id="31e6d-145">Klikk Parti.</span><span class="sxs-lookup"><span data-stu-id="31e6d-145">Click Batch.</span></span>
5. <span data-ttu-id="31e6d-146">Klikk på Ja for å aktivere satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="31e6d-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="31e6d-147">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="31e6d-147">Click Recurrence.</span></span>
7. <span data-ttu-id="31e6d-148">Velg Dager</span><span class="sxs-lookup"><span data-stu-id="31e6d-148">Select Days</span></span>
8. <span data-ttu-id="31e6d-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="31e6d-149">Click OK.</span></span>
9. <span data-ttu-id="31e6d-150">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="31e6d-150">Click OK.</span></span>
10. <span data-ttu-id="31e6d-151">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="31e6d-151">Click Cancel.</span></span>
11. <span data-ttu-id="31e6d-152">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="31e6d-152">Click Yes.</span></span>

