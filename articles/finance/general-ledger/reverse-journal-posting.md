---
title: Tilbakeføre journalpostering
description: Dette emnet beskriver funksjoner som lar deg tilbakeføre bilag fra bilagstransaksjonslisten eller fra finansjournaler.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5d1c58463c24dc6a40b036f0bb803316bbb65c2
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091905"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="a870e-103">Tilbakeføre journalpostering</span><span class="sxs-lookup"><span data-stu-id="a870e-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a870e-104">Dette emnet beskriver funksjonene i Microsoft Dynamics 365 Finance som lar deg tilbakeføre en hel journal eller tilbakeføre ett eller flere bilag fra bilagstransaksjonslisten, uavhengig av opprinnelsen.</span><span class="sxs-lookup"><span data-stu-id="a870e-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="a870e-105">Tilbakeføre journaler</span><span class="sxs-lookup"><span data-stu-id="a870e-105">Reversing journals</span></span>

<span data-ttu-id="a870e-106">Du kan tilbakeføre Journallinjer enkeltvis.</span><span class="sxs-lookup"><span data-stu-id="a870e-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="a870e-107">Med tilbakeføring av journalpostering kan du også tilbakeføre en hel finansjournal.</span><span class="sxs-lookup"><span data-stu-id="a870e-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="a870e-108">Slik tilbakefører du en journal:</span><span class="sxs-lookup"><span data-stu-id="a870e-108">To reverse a journal:</span></span> 

- <span data-ttu-id="a870e-109">Åpne finansjournalen, og filtrer på posterte journaler.</span><span class="sxs-lookup"><span data-stu-id="a870e-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="a870e-110">Velg **Tilbakefør**-menyen øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="a870e-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="a870e-111">Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført</span><span class="sxs-lookup"><span data-stu-id="a870e-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="a870e-112">Velg **Ja** hvis du vil bruke de eksisterende transaksjonsdatoene, eller **Nei** hvis du vil angi en ny.</span><span class="sxs-lookup"><span data-stu-id="a870e-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="a870e-113">I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket, og du må angi en ny transaksjonsdato for tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="a870e-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="a870e-114">Hvis du velger **Nei**, angir du en transaksjonsdato for tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="a870e-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="a870e-115">Angi en kommentar som du vil legge til i tilbakeføringstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="a870e-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="a870e-116">Velg **Tilbakeføring**-knappen.</span><span class="sxs-lookup"><span data-stu-id="a870e-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="a870e-117">Transaksjonen blir tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="a870e-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="a870e-118">Hvis antallet bilagslinjer overskrider 100 linjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen.</span><span class="sxs-lookup"><span data-stu-id="a870e-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="a870e-119">Du kan se gjennom resultatene ved å vise kommentarene i den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="a870e-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="a870e-120">Alle transaksjoner som ikke kan tilbakeføres, vises i loggen for den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="a870e-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="a870e-121">Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="a870e-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="a870e-122">Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres, sammen med årsaken til at det ikke kunne tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="a870e-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="a870e-123">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a870e-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="a870e-124">Tilbakeføring av bilag fra bilagstransaksjonslisten.</span><span class="sxs-lookup"><span data-stu-id="a870e-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="a870e-125">Du kan også tilbakeføre bilag fra **bilagstransaksjonslisten** på tvers av alle underfinansjournaler.</span><span class="sxs-lookup"><span data-stu-id="a870e-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="a870e-126">I tillegg kan du tilbakeføre flere enn ett bilag om gangen.</span><span class="sxs-lookup"><span data-stu-id="a870e-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="a870e-127">Slik tilbakefører du ett eller flere bilag:</span><span class="sxs-lookup"><span data-stu-id="a870e-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="a870e-128">Velg **Tilbakefør**-menyen øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="a870e-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="a870e-129">Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="a870e-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="a870e-130">Velg **Ja** hvis du vil bruke de eksisterende transaksjonsdatoene, eller **Nei** hvis du vil angi en ny.</span><span class="sxs-lookup"><span data-stu-id="a870e-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="a870e-131">I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket, og du må angi en ny transaksjonsdato for å tilbakeføre den.</span><span class="sxs-lookup"><span data-stu-id="a870e-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="a870e-132">Hvis du velger **Nei**, angir du en transaksjonsdato for tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="a870e-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="a870e-133">Angi en kommentar for å beskrive tilbakeføringstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="a870e-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="a870e-134">Velg **Tilbakeføring**-knappen.</span><span class="sxs-lookup"><span data-stu-id="a870e-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="a870e-135">Transaksjonen blir tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="a870e-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="a870e-136">Hvis det finnes mer enn 100 bilagslinjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen.</span><span class="sxs-lookup"><span data-stu-id="a870e-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="a870e-137">Du kan se gjennom resultatene ved å vise kommentarene i den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="a870e-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="a870e-138">Alle transaksjoner som ikke kan tilbakeføres, registreres i loggen for den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="a870e-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="a870e-139">Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="a870e-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="a870e-140">Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres, sammen med årsaken til at det ikke kunne tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="a870e-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="a870e-141">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a870e-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="a870e-142">Transaksjoner kan bare tilbakeføres hvis de oppfyller forretningsreglene for tilbakeføring.</span><span class="sxs-lookup"><span data-stu-id="a870e-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="a870e-143">Leverandørbetalinger kan ikke reverseres ved hjelp av funksjonen som er beskrevet i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="a870e-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="a870e-144">Leverandørbetalinger må tilbakeføres ved å følge fremgangsmåten i [Tilbakeføre en leverandørbetaling](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="a870e-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

