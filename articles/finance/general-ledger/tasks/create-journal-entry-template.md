---
title: Opprette en journaloppføring ved hjelp av en mal
description: Posterte journalbilag kan lagres som bilagsmaler og brukes i et nytt journalbilag.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 360df29e6349fd4d42d6d14af646e929b73943bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145169"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="86f22-103">Opprette en journaloppføring ved hjelp av en mal</span><span class="sxs-lookup"><span data-stu-id="86f22-103">Create a journal entry using template</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86f22-104">Posterte journalbilag kan lagres som bilagsmaler og brukes i et nytt journalbilag.</span><span class="sxs-lookup"><span data-stu-id="86f22-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="86f22-105">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="86f22-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="86f22-106">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Journaloppføringer > Økonomijournaler**.</span><span class="sxs-lookup"><span data-stu-id="86f22-106">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
2. <span data-ttu-id="86f22-107">Klikk **Ny** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="86f22-107">On the **Action pane**, click **New**.</span></span> <span data-ttu-id="86f22-108">Denne prosedyren starter ved å opprette og postere et journalbilag, men eventuelle tidligere posterte journalbilag kan lagres som en mal.</span><span class="sxs-lookup"><span data-stu-id="86f22-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
3. <span data-ttu-id="86f22-109">Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="86f22-109">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="86f22-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="86f22-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="86f22-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="86f22-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="86f22-112">Klikk **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="86f22-112">Click **Lines**.</span></span>
7. <span data-ttu-id="86f22-113">Angi en verdi i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="86f22-113">In the **Account type** field, type a value.</span></span>
8. <span data-ttu-id="86f22-114">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="86f22-114">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="86f22-115">Skriv inn en verdi i **Debet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="86f22-115">In the **Debit** field, type a value.</span></span>
10. <span data-ttu-id="86f22-116">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="86f22-116">Click **New**.</span></span>
11. <span data-ttu-id="86f22-117">Angi en verdi i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="86f22-117">In the **Account type** field, type a value.</span></span>
12. <span data-ttu-id="86f22-118">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="86f22-118">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="86f22-119">Skriv inn en verdi i **Debet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="86f22-119">In the **Debit** field, type a value.</span></span>
14. <span data-ttu-id="86f22-120">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="86f22-120">Click **New**.</span></span>
14. <span data-ttu-id="86f22-121">Angi de ønskede verdiene i **Konto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="86f22-121">In the **Account** field, specify the desired values.</span></span>
15. <span data-ttu-id="86f22-122">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="86f22-122">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="86f22-123">Skriv inn en verdi i **Kredit**-feltet for å balansere bilaget.</span><span class="sxs-lookup"><span data-stu-id="86f22-123">In the **Credit** field, type a value to balance the voucher.</span></span>
17. <span data-ttu-id="86f22-124">Klikk **Poster** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="86f22-124">On the **Action pane**, click **Post**.</span></span>
18. <span data-ttu-id="86f22-125">Klikk **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="86f22-125">Click **Functions**.</span></span>
19. <span data-ttu-id="86f22-126">Klikk **Lagre bilag som mal**.</span><span class="sxs-lookup"><span data-stu-id="86f22-126">Click **Save voucher** template.</span></span>
20. <span data-ttu-id="86f22-127">Denne fremgangsmåten forutsetter en **maltype som prosent**.</span><span class="sxs-lookup"><span data-stu-id="86f22-127">This procedure assumes a **Percent Template** type.</span></span> <span data-ttu-id="86f22-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="86f22-128">Click OK.</span></span>
    - <span data-ttu-id="86f22-129">Prosent: beløpene i bilaget konverteres til prosentfaktorer, som gjør at alle beløp kan brukes når bilagsmalen er valgt.</span><span class="sxs-lookup"><span data-stu-id="86f22-129">Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>
    - <span data-ttu-id="86f22-130">Beløp: de faktiske beløpene lagres og brukes.</span><span class="sxs-lookup"><span data-stu-id="86f22-130">Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="86f22-131">Klikk **Økonomijournaler**.</span><span class="sxs-lookup"><span data-stu-id="86f22-131">Click **General journals**.</span></span>
22. <span data-ttu-id="86f22-132">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="86f22-132">Click **New**.</span></span>
23. <span data-ttu-id="86f22-133">Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="86f22-133">In the **Name** field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="86f22-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="86f22-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="86f22-135">Klikk **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="86f22-135">Click **Lines**.</span></span>
26. <span data-ttu-id="86f22-136">Klikk **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="86f22-136">Click **Functions**.</span></span>
27. <span data-ttu-id="86f22-137">Klikk **Velg bilagsmal**.</span><span class="sxs-lookup"><span data-stu-id="86f22-137">Click **Select voucher template**.</span></span>
28. <span data-ttu-id="86f22-138">Finn malen som du opprettet før.</span><span class="sxs-lookup"><span data-stu-id="86f22-138">Find the template that you created earlier.</span></span> <span data-ttu-id="86f22-139">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="86f22-139">Click **OK**.</span></span> <span data-ttu-id="86f22-140">Du må kanskje klikke **Forrige trinn** og deretter velge riktig mal hvis det finnes andre maler.</span><span class="sxs-lookup"><span data-stu-id="86f22-140">You may need to click **Previous step** and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="86f22-141">I feltet **Beløp** kan du angi beløpet som skal brukes for bilaget.</span><span class="sxs-lookup"><span data-stu-id="86f22-141">In the **Amount** field, enter the amount to be applied to the voucher.</span></span> <span data-ttu-id="86f22-142">**Beløp**-feltet vises bare hvis bilagsmalen er av typen Prosent.</span><span class="sxs-lookup"><span data-stu-id="86f22-142">The **Amount** field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="86f22-143">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="86f22-143">Click **OK**.</span></span>

