---
title: Registrere fakturadata i Leverandører ved hjelp av en godkjenningsjournal
description: Dette emnet forklarer hvordan du bruker ankomstregistreringen til å opprette fakturaer, og deretter bruke godkjenningsjournalen for å oppdatere utgiftskontoene.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb690769a33f88e63ab8f54cec69a5e927fd324c
ms.sourcegitcommit: 6545bef4584d72dd7789f2d3935cf00ac8f489b0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2019
ms.locfileid: "1871011"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="4d309-103">Registrere fakturadata i Leverandører ved hjelp av en godkjenningsjournal</span><span class="sxs-lookup"><span data-stu-id="4d309-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d309-104">Dette emnet forklarer hvordan du bruker ankomstregistreringen til å opprette fakturaer, og deretter bruke godkjenningsjournalen for å oppdatere utgiftskontoene.</span><span class="sxs-lookup"><span data-stu-id="4d309-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="4d309-105">Opprette og postere en faktura</span><span class="sxs-lookup"><span data-stu-id="4d309-105">Create and post and invoice</span></span>
1. <span data-ttu-id="4d309-106">Gå til **Moduler > Leverandører > Fakturaer > Ankomstregistrering** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="4d309-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="4d309-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4d309-107">Select **New**.</span></span>
3. <span data-ttu-id="4d309-108">Velg navnet på ankomstregistreringen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="4d309-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="4d309-109">Velg **Linjer** for å åpne registeret og angi utgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="4d309-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="4d309-110">Velg en leverandør.</span><span class="sxs-lookup"><span data-stu-id="4d309-110">Select a vendor.</span></span> <span data-ttu-id="4d309-111">Du kan for eksempel angi eller velge `US-104`.</span><span class="sxs-lookup"><span data-stu-id="4d309-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="4d309-112">Skriv inn en verdi i **Faktura**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d309-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="4d309-113">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d309-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="4d309-114">Angi et tall i **Kredit**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d309-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="4d309-115">I **Godkjent av**-feltet velger du en godkjenner fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="4d309-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="4d309-116">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="4d309-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="4d309-117">Godkjenne en faktura</span><span class="sxs-lookup"><span data-stu-id="4d309-117">Approve an invoice</span></span>
1. <span data-ttu-id="4d309-118">Gå til **Moduler > Leverandører > Fakturaer > Fakturagodkjenning** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="4d309-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="4d309-119">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4d309-119">Select **New**.</span></span>
3. <span data-ttu-id="4d309-120">Velg navnet på fakturagodkjenningsjournalen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="4d309-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="4d309-121">Velg **Linjer** for å vise en side der du kan velge fakturaene som du vil godkjenne.</span><span class="sxs-lookup"><span data-stu-id="4d309-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="4d309-122">Velg **Finn bilag** for å vise alle fakturaer som er klare til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="4d309-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="4d309-123">Merk fakturaen som du opprettet, og klikk deretter på **Velg** .</span><span class="sxs-lookup"><span data-stu-id="4d309-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="4d309-124">Bilagene som du valgte ovenfor, flyttes til denne listen når du merker dem.</span><span class="sxs-lookup"><span data-stu-id="4d309-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="4d309-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d309-125">Select **OK**.</span></span>
8. <span data-ttu-id="4d309-126">Velg **kontonummer**-feltet for å legge til en utgiftskonto i fakturaen.</span><span class="sxs-lookup"><span data-stu-id="4d309-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="4d309-127">Skriv inn et kontonummer og gå ut av feltet.</span><span class="sxs-lookup"><span data-stu-id="4d309-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="4d309-128">Skriv for eksempel inn `600120`.</span><span class="sxs-lookup"><span data-stu-id="4d309-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="4d309-129">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="4d309-129">Select **Post**.</span></span>
11. <span data-ttu-id="4d309-130">Velg **Bilag** for å vise oppføringene som ble postert.</span><span class="sxs-lookup"><span data-stu-id="4d309-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="4d309-131">Kontoen for fakturaen som venter på godkjenning, tilbakeføres og erstattes med den faktiske utgiftskontoen.</span><span class="sxs-lookup"><span data-stu-id="4d309-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

