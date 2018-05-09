---
title: Avstemme frakt i transportstyring
description: Denne artikkelen beskriver fraktavstemmingsprosessen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c52d92b08c2832541fbebe2bf14c942bb79b1540
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="e1531-103">Avstemme frakt i transportstyring</span><span class="sxs-lookup"><span data-stu-id="e1531-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1531-104">Denne artikkelen beskriver fraktavstemmingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="e1531-104">This article describes the freight reconciliation process.</span></span>

<span data-ttu-id="e1531-105">Fraktavstemming kan gjøres manuelt, eller det kan settes opp til å skje automatisk.</span><span class="sxs-lookup"><span data-stu-id="e1531-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="e1531-106">Hvis du vil bruke automatisk fraktavstemming, må du opprette en revisjonsstandard der du kan definere kriteriene som bestemmer hvilke fraktbrev som sammenlignes automatisk.</span><span class="sxs-lookup"><span data-stu-id="e1531-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="e1531-107">Fraktavstemmingsprosessen</span><span class="sxs-lookup"><span data-stu-id="e1531-107">The freight reconciliation process</span></span>
<span data-ttu-id="e1531-108">Fraktsatser beregnes av satsmotoren som er tilknyttet med den aktuelle transportøren.</span><span class="sxs-lookup"><span data-stu-id="e1531-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="e1531-109">Når en last er bekreftet, genereres et fraktbrev og fraktsatser overføres til den.</span><span class="sxs-lookup"><span data-stu-id="e1531-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="e1531-110">Fraktsatsene fordeles som tillegg til det aktuelle kildedokumentet (bestilling, salgsordre, og/eller overføringsordre), avhengig av oppsettet som brukes for den vanlige faktureringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="e1531-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="e1531-111">Fraktavstemmingsprosessen (som også kalles kontrollprosessen) kan starte så snart fraktfakturaen mottas fra transportøren.</span><span class="sxs-lookup"><span data-stu-id="e1531-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="e1531-112">Fakturaen kan mottas elektronisk eller på papir.</span><span class="sxs-lookup"><span data-stu-id="e1531-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="e1531-113">Hvis fakturaen mottas på papir, kan du generere en elektronisk faktura ved hjelp av fraktbrevet som mal.</span><span class="sxs-lookup"><span data-stu-id="e1531-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="e1531-114">[![Fraktavstemmingsprosessen](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="e1531-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="e1531-115">Manuell avstemming</span><span class="sxs-lookup"><span data-stu-id="e1531-115">Manual reconciliation</span></span>
<span data-ttu-id="e1531-116">Hvis du er avstemmer frakt manuelt, må du sammenligne hver fakturalinje med fraktbrevlinjen eller -linjene for lasten som skal faktureres.</span><span class="sxs-lookup"><span data-stu-id="e1531-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="e1531-117">Du gjør dette på siden **Samsvare fraktbrev og faktura**.</span><span class="sxs-lookup"><span data-stu-id="e1531-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="e1531-118">Hvis beløpet på fakturalinjen ikke samsvarer med hvor fraktbrevbeløpet, må du velge en avstemmingsårsak for forskjellen.</span><span class="sxs-lookup"><span data-stu-id="e1531-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="e1531-119">Hvis det er flere årsaker til avstemming, kan du dele de ikke-samsvarte beløpene på tvers av dem.</span><span class="sxs-lookup"><span data-stu-id="e1531-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="e1531-120">Årsaken til avstemming bestemmer hvordan differansebeløpene posteres i Finans.</span><span class="sxs-lookup"><span data-stu-id="e1531-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="e1531-121">Når avstemmingen av hele fakturabeløpet er gjort rede for, sendes sendt til godkjenning, og deretter posteres journalen.</span><span class="sxs-lookup"><span data-stu-id="e1531-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="e1531-122">Illustrasjonen nedenfor viser hvordan du genererer en fraktfaktura og utfører fraktavstemming i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1531-122">The following illustration shows how to generate a freight invoice and do freight reconciliation in Microsoft Dynamics 365 for Finance and Operations.</span></span> 
<span data-ttu-id="e1531-123">[![Fraktavstemmingsoppgaver i Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="e1531-123">[![Freight reconcilation tasks in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="e1531-124">Automatisk avstemming</span><span class="sxs-lookup"><span data-stu-id="e1531-124">Automatic reconciliation</span></span>
<span data-ttu-id="e1531-125">Hvis du vil bruke automatisk avstemming, må du angi tidsplanen for avstemming og fakturaene og transportørene som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="e1531-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="e1531-126">Treff for fakturalinjer og fraktbrev gjøres i henhold til oppsettet av typen revisjonsstandard og fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="e1531-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="e1531-127">Når du har kjørt automatisk avstemming, må du håndtere alle fakturaer som systemet ikke kan samsvare.</span><span class="sxs-lookup"><span data-stu-id="e1531-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="e1531-128">Du må behandle disse fakturaene manuelt før du kan bokføre alle fakturaene for betaling.</span><span class="sxs-lookup"><span data-stu-id="e1531-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>




