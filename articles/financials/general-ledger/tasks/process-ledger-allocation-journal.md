--- 
title: Behandle finansfordelingsjournal
description: "Bruk siden Behandle tildelingsforespørsel for å opprette en tildelingsjournal som kan du kan vurdere og godkjenne før du posterer den til økonomimodul, eller posterer direkte til økonomimodul."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7d299657758b1e1322aef07bfe8c71f7bf00b0ca
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="a70ed-103">Behandle finansfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="a70ed-103">Process ledger allocation journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a70ed-104">Bruk siden Behandle tildelingsforespørsel for å opprette en tildelingsjournal som kan du kan vurdere og godkjenne før du posterer den til økonomimodul, eller posterer direkte til økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="a70ed-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="a70ed-105">Før du kan opprette en tildelingsjournal, må det være minst én aktiv tildelingsregel for finans.</span><span class="sxs-lookup"><span data-stu-id="a70ed-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="a70ed-106">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="a70ed-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a70ed-107">Gå til Økonomimodul > Tildelinger > Behandle tildelingsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="a70ed-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="a70ed-108">Klikk rullegardinknappen i feltet Regel for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a70ed-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a70ed-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="a70ed-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a70ed-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a70ed-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a70ed-111">Angi en dato i Per dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="a70ed-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="a70ed-112">Per dato er svært viktig når finans er datakilden for regelen.</span><span class="sxs-lookup"><span data-stu-id="a70ed-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="a70ed-113">Denne datoen kontrollerer hvilke finanssaldoer som skal inkluderes i tildelingen.</span><span class="sxs-lookup"><span data-stu-id="a70ed-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="a70ed-114">Velg Stopp i Nullkilde-feltet.</span><span class="sxs-lookup"><span data-stu-id="a70ed-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="a70ed-115">Dette vil stanse tildelingsprosessen og vise en melding som indikerer at et nullbeløp er valgt.</span><span class="sxs-lookup"><span data-stu-id="a70ed-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="a70ed-116">I feltet Forslagsalternativer velger du "Bare forslag".</span><span class="sxs-lookup"><span data-stu-id="a70ed-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="a70ed-117">Velg Bare forslag for å se gjennom og eventuelt godkjenne resultatet i tildelingsjournaler før postering av tildelingen til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="a70ed-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="a70ed-118">Angi en dato i feltet FIN-posteringsdato.</span><span class="sxs-lookup"><span data-stu-id="a70ed-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="a70ed-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a70ed-119">Click OK.</span></span>
9. <span data-ttu-id="a70ed-120">Gå til Økonomimodul > Tildelinger > Tildelingsjournaler.</span><span class="sxs-lookup"><span data-stu-id="a70ed-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="a70ed-121">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="a70ed-121">Click Lines.</span></span>
11. <span data-ttu-id="a70ed-122">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="a70ed-122">Click Post.</span></span>
12. <span data-ttu-id="a70ed-123">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="a70ed-123">Click Post.</span></span>


