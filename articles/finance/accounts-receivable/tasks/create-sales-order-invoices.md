---
title: Opprette salgsordrefakturaer
description: Denne oppgaveveiledningen beskriver fakturering av salgsordren, inkludert fletting av fakturaer og satsvis behandling.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0076e838ad4eac687dc7db1bc0a94891f0ee6d9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991023"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="c209e-103">Opprette salgsordrefakturaer</span><span class="sxs-lookup"><span data-stu-id="c209e-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c209e-104">Denne oppgaveveiledningen beskriver fakturering av salgsordren, inkludert fletting av fakturaer og satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="c209e-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="c209e-105">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="c209e-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="c209e-106">Opprette en faktura fra en salgsordre</span><span class="sxs-lookup"><span data-stu-id="c209e-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="c209e-107">Gå til **Navigasjonsrute > Moduler > Kunder > Ordrer > Salgsordrer som er sendt, men ikke fakturert**.</span><span class="sxs-lookup"><span data-stu-id="c209e-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="c209e-108">Velg en salgsordre fra listen.</span><span class="sxs-lookup"><span data-stu-id="c209e-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="c209e-109">Klikk på **Faktura > Generer > Faktura** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="c209e-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="c209e-110">Legg merke til at denne salgsordren har flere følgesedler tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="c209e-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="c209e-111">Den viser bare ordet <multiple> i stedet for følgeseddelnummeret.</span><span class="sxs-lookup"><span data-stu-id="c209e-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="c209e-112">Utvid seksjonen **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="c209e-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="c209e-113">Postering må settes til Ja for å postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="c209e-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="c209e-114">Du kan også slå av postering, og du kan bare skrive ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="c209e-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="c209e-115">Du kan imidlertid oppnå samme resultat ved å opprette en proformafaktura i stedet for en faktura.</span><span class="sxs-lookup"><span data-stu-id="c209e-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="c209e-116">Dette alternativet brukes for satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="c209e-116">This option is used for batch jobs.</span></span> <span data-ttu-id="c209e-117">Spørringen kjøres når den satsvise jobben kjøres.</span><span class="sxs-lookup"><span data-stu-id="c209e-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="c209e-118">Velg Etter i feltet **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="c209e-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="c209e-119">Velg **Ja** for **Skriv ut faktura**.</span><span class="sxs-lookup"><span data-stu-id="c209e-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="c209e-120">Utskriftsbehandling kan skrive ut flere eksemplarer av fakturaen, og også sende fakturaen via e-post som en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="c209e-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="c209e-121">Velg Summer i feltet **Skriv ut tillegg**.</span><span class="sxs-lookup"><span data-stu-id="c209e-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="c209e-122">I feltet **Kontroller kredittgrense** velger du Saldo.</span><span class="sxs-lookup"><span data-stu-id="c209e-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="c209e-123">Klikk på **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="c209e-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="c209e-124">Kombinere ordrer til én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="c209e-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="c209e-125">Gå til **Navigasjonsrute > Moduler > Kunder > Ordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="c209e-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="c209e-126">Finn en kunde som har flere fakturaer som er åpne.</span><span class="sxs-lookup"><span data-stu-id="c209e-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="c209e-127">Velg flere åpne salgsordrer fra samme kunde.</span><span class="sxs-lookup"><span data-stu-id="c209e-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="c209e-128">Klikk på **Faktura > Generer > Faktura** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="c209e-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="c209e-129">Utvid seksjonen **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="c209e-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="c209e-130">Velg Alle i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c209e-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="c209e-131">Legg merke til at det finnes to fakturaer som er oppført i oversiktsdelen.</span><span class="sxs-lookup"><span data-stu-id="c209e-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="c209e-132">Nå skal vi slå dem sammen til én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="c209e-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="c209e-133">I feltet **Samleoppdatering for** velger du Fakturakonto.</span><span class="sxs-lookup"><span data-stu-id="c209e-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="c209e-134">Klikk på **Ordne** for å slå sammen salgsordrene til én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="c209e-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="c209e-135">De to ordrene er nå slått sammen til én enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="c209e-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="c209e-136">Klikk på **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="c209e-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="c209e-137">Klikk **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c209e-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="c209e-138">Postere fakturaer i en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="c209e-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="c209e-139">Gå til **Navigasjonsrute > Moduler > Kunder > Fakturaer > Partifakturering > Faktura**.</span><span class="sxs-lookup"><span data-stu-id="c209e-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="c209e-140">Klikk **Velg**.</span><span class="sxs-lookup"><span data-stu-id="c209e-140">Click **Select**.</span></span>
3. <span data-ttu-id="c209e-141">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c209e-141">Click **OK**.</span></span>
4. <span data-ttu-id="c209e-142">Klikk på **Parti**.</span><span class="sxs-lookup"><span data-stu-id="c209e-142">Click **Batch**.</span></span>
5. <span data-ttu-id="c209e-143">Velg **Ja** i **Satsvis behandling**.</span><span class="sxs-lookup"><span data-stu-id="c209e-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="c209e-144">Klikk på **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="c209e-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="c209e-145">Velg **Dager**.</span><span class="sxs-lookup"><span data-stu-id="c209e-145">Select **Days**.</span></span>
8. <span data-ttu-id="c209e-146">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c209e-146">Click **OK**.</span></span>
9. <span data-ttu-id="c209e-147">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c209e-147">Click **OK**.</span></span>
10. <span data-ttu-id="c209e-148">Klikk på **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="c209e-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="c209e-149">Klikk **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c209e-149">Click **Yes**.</span></span>

