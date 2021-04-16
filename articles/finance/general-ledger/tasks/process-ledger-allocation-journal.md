---
title: Behandle finansfordelingsjournal
description: Dette emnet beskriver hvordan du behandler en tildelingsforespørsel i Dynamics 365 Finance.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e89aa21f988d50bc1a922e053be0ff2dcd196268
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834428"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="828bd-103">Behandle finansfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="828bd-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="828bd-104">Dette emnet beskriver hvordan du behandler en tildelingsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="828bd-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="828bd-105">Bruk siden Behandle tildelingsforespørsel for å opprette en tildelingsjournal som kan du kan vurdere og godkjenne før du posterer den til økonomimodul, eller posterer direkte til økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="828bd-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="828bd-106">Før du kan opprette en tildelingsjournal, må det være minst én aktiv tildelingsregel for finans.</span><span class="sxs-lookup"><span data-stu-id="828bd-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="828bd-107">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="828bd-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="828bd-108">Gå til **Moduler > Økonomimodul > Tildelinger > Behandle tildelingsforespørsel** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="828bd-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="828bd-109">Velg det ønskede oppslaget på rullegardinmenyen i **Regel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="828bd-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="828bd-110">Angi en dato i **Per dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="828bd-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="828bd-111">**Per dato** er svært viktig når finans er datakilden for regelen.</span><span class="sxs-lookup"><span data-stu-id="828bd-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="828bd-112">Denne datoen kontrollerer hvilke finanssaldoer som skal inkluderes i tildelingen.</span><span class="sxs-lookup"><span data-stu-id="828bd-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="828bd-113">Velg **Stopp** i **Nullkilde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="828bd-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="828bd-114">Dette vil stanse tildelingsprosessen og vise en melding som indikerer at et nullbeløp er valgt.</span><span class="sxs-lookup"><span data-stu-id="828bd-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="828bd-115">I feltet **Forslagsalternativer** velger du **Bare forslag**.</span><span class="sxs-lookup"><span data-stu-id="828bd-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="828bd-116">Velg **Bare forslag** for å se gjennom og eventuelt godkjenne resultatet i tildelingsjournaler før postering av tildelingen til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="828bd-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="828bd-117">Angi en dato i feltet FIN-posteringsdato.</span><span class="sxs-lookup"><span data-stu-id="828bd-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="828bd-118">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="828bd-118">Select **OK**.</span></span>
7. <span data-ttu-id="828bd-119">Gå til **Moduler > Økonomimodul > Tildelinger > Fordelingsjournaler** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="828bd-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="828bd-120">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="828bd-120">Select **Lines**.</span></span>
9. <span data-ttu-id="828bd-121">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="828bd-121">Select **Post**.</span></span>
10. <span data-ttu-id="828bd-122">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="828bd-122">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]