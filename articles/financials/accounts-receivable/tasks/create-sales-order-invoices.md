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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba8e0f02f2d1eb12cecc2c434fbca1e198cddbe9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842959"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="a678a-103">Opprette salgsordrefakturaer</span><span class="sxs-lookup"><span data-stu-id="a678a-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a678a-104">Denne oppgaveveiledningen beskriver fakturering av salgsordren, inkludert fletting av fakturaer og satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="a678a-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="a678a-105">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="a678a-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="a678a-106">Opprette en faktura fra en salgsordre</span><span class="sxs-lookup"><span data-stu-id="a678a-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="a678a-107">Gå til Kunder > Ordrer > Salgsordrer som er sendt, men ikke fakturert.</span><span class="sxs-lookup"><span data-stu-id="a678a-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="a678a-108">Velg en salgsordre fra listen.</span><span class="sxs-lookup"><span data-stu-id="a678a-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="a678a-109">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a678a-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="a678a-110">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="a678a-110">Click Invoice.</span></span>
    * <span data-ttu-id="a678a-111">Legg merke til at denne salgsordren har flere følgesedler tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="a678a-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="a678a-112">Den viser bare ordet <multiple> i stedet for følgeseddelnummeret.</span><span class="sxs-lookup"><span data-stu-id="a678a-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="a678a-113">Utvid seksjonen Parametere.</span><span class="sxs-lookup"><span data-stu-id="a678a-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="a678a-114">Postering må settes til Ja for å postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a678a-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="a678a-115">Du kan også slå av postering, og du kan bare skrive ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a678a-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="a678a-116">Du kan imidlertid oppnå samme resultat ved å opprette en proformafaktura i stedet for en faktura.</span><span class="sxs-lookup"><span data-stu-id="a678a-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="a678a-117">Dette alternativet brukes for satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="a678a-117">This option is used for batch jobs.</span></span> <span data-ttu-id="a678a-118">Spørringen kjøres når den satsvise jobben kjøres.</span><span class="sxs-lookup"><span data-stu-id="a678a-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="a678a-119">Velg Etter i feltet Skriv ut.</span><span class="sxs-lookup"><span data-stu-id="a678a-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="a678a-120">Velg Ja for å skrive ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a678a-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="a678a-121">Utskriftsbehandling kan skrive ut flere eksemplarer av fakturaen, og også sende fakturaen via e-post som en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="a678a-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="a678a-122">Velg Summer i feltet Skriv ut tillegg.</span><span class="sxs-lookup"><span data-stu-id="a678a-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="a678a-123">I feltet Kontroller kredittgrense velger du Saldo.</span><span class="sxs-lookup"><span data-stu-id="a678a-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="a678a-124">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="a678a-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="a678a-125">Kombinere ordrer til én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="a678a-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="a678a-126">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="a678a-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="a678a-127">Finn en kunde som har flere fakturaer som er åpne.</span><span class="sxs-lookup"><span data-stu-id="a678a-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="a678a-128">Velg en åpen salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a678a-128">Select an open sales order.</span></span>
4. <span data-ttu-id="a678a-129">Velg en ny åpen salgsordre for den samme kunden.</span><span class="sxs-lookup"><span data-stu-id="a678a-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="a678a-130">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a678a-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="a678a-131">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="a678a-131">Click Invoice.</span></span>
7. <span data-ttu-id="a678a-132">Utvid seksjonen Parametere.</span><span class="sxs-lookup"><span data-stu-id="a678a-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="a678a-133">Velg Alle i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="a678a-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="a678a-134">Legg merke til at det finnes to fakturaer som er oppført i oversiktsdelen.</span><span class="sxs-lookup"><span data-stu-id="a678a-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="a678a-135">Nå skal vi slå dem sammen til én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="a678a-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="a678a-136">I samleoppdateringen for feltet velger du "Fakturakonto".</span><span class="sxs-lookup"><span data-stu-id="a678a-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="a678a-137">Klikk Ordre for å slå sammen salgsordrene til én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="a678a-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="a678a-138">De to ordrene er nå slått sammen til én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="a678a-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="a678a-139">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="a678a-139">Click Cancel.</span></span>
12. <span data-ttu-id="a678a-140">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="a678a-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="a678a-141">Postere fakturaer i en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="a678a-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="a678a-142">Gå til Kunder > Fakturaer > Partifakturering > Faktura.</span><span class="sxs-lookup"><span data-stu-id="a678a-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="a678a-143">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="a678a-143">Click Select.</span></span>
3. <span data-ttu-id="a678a-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a678a-144">Click OK.</span></span>
4. <span data-ttu-id="a678a-145">Klikk Parti.</span><span class="sxs-lookup"><span data-stu-id="a678a-145">Click Batch.</span></span>
5. <span data-ttu-id="a678a-146">Klikk på Ja for å aktivere satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="a678a-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="a678a-147">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="a678a-147">Click Recurrence.</span></span>
7. <span data-ttu-id="a678a-148">Velg Dager</span><span class="sxs-lookup"><span data-stu-id="a678a-148">Select Days</span></span>
8. <span data-ttu-id="a678a-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a678a-149">Click OK.</span></span>
9. <span data-ttu-id="a678a-150">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a678a-150">Click OK.</span></span>
10. <span data-ttu-id="a678a-151">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="a678a-151">Click Cancel.</span></span>
11. <span data-ttu-id="a678a-152">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="a678a-152">Click Yes.</span></span>

