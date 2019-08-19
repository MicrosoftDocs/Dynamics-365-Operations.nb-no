---
title: Hovedfakturadata inn i AP-systemet ved hjelp av godkjenningsjournal
description: Denne oppgaveveiledningen viser hvordan du bruker ankomstregistreringen til opprette fakturaer, og deretter bruke godkjenningsjournalen for å oppdatere utgiftskontoene.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 0faece510cc85fd86113d8b62d54b71f3014b1db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837051"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="d09ee-103">Hovedfakturadata inn i AP-systemet ved hjelp av godkjenningsjournal</span><span class="sxs-lookup"><span data-stu-id="d09ee-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d09ee-104">Denne oppgaveveiledningen viser hvordan du bruker ankomstregistreringen til opprette fakturaer, og deretter bruke godkjenningsjournalen for å oppdatere utgiftskontoene.</span><span class="sxs-lookup"><span data-stu-id="d09ee-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="d09ee-105">Opprette og postere en faktura</span><span class="sxs-lookup"><span data-stu-id="d09ee-105">Create and post and invoice</span></span>
1. <span data-ttu-id="d09ee-106">Gå til Leverandører > Fakturaer > Ankomstregistrering.</span><span class="sxs-lookup"><span data-stu-id="d09ee-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="d09ee-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d09ee-107">Click New.</span></span>
3. <span data-ttu-id="d09ee-108">Velg navnet på ankomstregistreringen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="d09ee-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="d09ee-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d09ee-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d09ee-110">Klikk Linjer for å åpne registeret og angi utgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="d09ee-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="d09ee-111">Velg en leverandør.</span><span class="sxs-lookup"><span data-stu-id="d09ee-111">Select a vendor.</span></span> <span data-ttu-id="d09ee-112">Du kan for eksempel angi eller velge USA – 104</span><span class="sxs-lookup"><span data-stu-id="d09ee-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="d09ee-113">Skriv inn en verdi i Faktura-feltet.</span><span class="sxs-lookup"><span data-stu-id="d09ee-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="d09ee-114">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="d09ee-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="d09ee-115">Angi et tall i Kredit-feltet.</span><span class="sxs-lookup"><span data-stu-id="d09ee-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="d09ee-116">Klikk rullegardinknappen i Godkjent av-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d09ee-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d09ee-117">Merk en godkjenner, og klikk Velg for å velge denne godkjenneren.</span><span class="sxs-lookup"><span data-stu-id="d09ee-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="d09ee-118">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="d09ee-118">Click Post.</span></span>
13. <span data-ttu-id="d09ee-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d09ee-119">Close the page.</span></span>
14. <span data-ttu-id="d09ee-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d09ee-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="d09ee-121">Godkjenne en faktura</span><span class="sxs-lookup"><span data-stu-id="d09ee-121">Approve an invoice</span></span>
1. <span data-ttu-id="d09ee-122">Gå til Leverandører > Fakturaer > Fakturagodkjenning.</span><span class="sxs-lookup"><span data-stu-id="d09ee-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="d09ee-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d09ee-123">Click New.</span></span>
3. <span data-ttu-id="d09ee-124">Velg navnet på fakturagodkjenningsjournalen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="d09ee-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="d09ee-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d09ee-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d09ee-126">Klikk linjer for å vise en side der du kan velge fakturaene som du vil godkjenne.</span><span class="sxs-lookup"><span data-stu-id="d09ee-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="d09ee-127">Velg Finn bilag for å vise alle fakturaer som er klare til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="d09ee-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="d09ee-128">Merk fakturaen som du opprettet.</span><span class="sxs-lookup"><span data-stu-id="d09ee-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="d09ee-129">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="d09ee-129">Click Select.</span></span>
    * <span data-ttu-id="d09ee-130">Bilagene som du valgte ovenfor, flyttes til denne listen når du merker dem.</span><span class="sxs-lookup"><span data-stu-id="d09ee-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="d09ee-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="d09ee-131">Click OK.</span></span>
10. <span data-ttu-id="d09ee-132">Klikk på kontonummerfeltet for å legge til en utgiftskonto i fakturaen.</span><span class="sxs-lookup"><span data-stu-id="d09ee-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="d09ee-133">Skriv inn et kontonummer og gå ut av feltet.</span><span class="sxs-lookup"><span data-stu-id="d09ee-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="d09ee-134">Skriv for eksempel inn 600120.</span><span class="sxs-lookup"><span data-stu-id="d09ee-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="d09ee-135">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="d09ee-135">Click Post.</span></span>
13. <span data-ttu-id="d09ee-136">Velg Bilag for å vise oppføringene som ble postert.</span><span class="sxs-lookup"><span data-stu-id="d09ee-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="d09ee-137">Kontoen for fakturaen som venter på godkjenning, tilbakeføres og erstattes med den faktiske utgiftskontoen.</span><span class="sxs-lookup"><span data-stu-id="d09ee-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

