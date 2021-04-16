---
title: Tilbakeføre journalpostering
description: Dette emnet beskriver funksjoner som lar deg tilbakeføre bilag fra bilagstransaksjonslisten eller fra finansjournaler.
author: MikeFalkner
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 586c0f807cf45908bacd88ff4e4d5793db054e4d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815410"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="3d8fc-103">Tilbakeføre journalpostering</span><span class="sxs-lookup"><span data-stu-id="3d8fc-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d8fc-104">Dette emnet beskriver funksjonene i Microsoft Dynamics 365 Finance som lar deg tilbakeføre en hel journal eller tilbakeføre ett eller flere bilag fra bilagstransaksjonslisten, uavhengig av opprinnelsen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="3d8fc-105">Tilbakeføre journaler</span><span class="sxs-lookup"><span data-stu-id="3d8fc-105">Reversing journals</span></span>

<span data-ttu-id="3d8fc-106">Du kan tilbakeføre Journallinjer enkeltvis.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="3d8fc-107">Med tilbakeføring av journalpostering kan du også tilbakeføre en hel finansjournal.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="3d8fc-108">Slik tilbakefører du en journal:</span><span class="sxs-lookup"><span data-stu-id="3d8fc-108">To reverse a journal:</span></span> 

- <span data-ttu-id="3d8fc-109">Åpne finansjournalen, og filtrer på posterte journaler.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="3d8fc-110">Velg **Tilbakefør**-menyen øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="3d8fc-111">Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført</span><span class="sxs-lookup"><span data-stu-id="3d8fc-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="3d8fc-112">Velg **Ja** hvis du vil bruke de eksisterende transaksjonsdatoene, eller **Nei** hvis du vil angi en ny.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="3d8fc-113">I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket, og du må angi en ny transaksjonsdato for tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="3d8fc-114">Hvis du velger **Nei**, angir du en transaksjonsdato for tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="3d8fc-115">Angi en kommentar som du vil legge til i tilbakeføringstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="3d8fc-116">Velg **Tilbakeføring**-knappen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="3d8fc-117">Transaksjonen blir tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="3d8fc-118">Hvis antallet bilagslinjer overskrider 100 linjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="3d8fc-119">Du kan se gjennom resultatene ved å vise kommentarene i den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="3d8fc-120">Alle transaksjoner som ikke kan tilbakeføres, vises i loggen for den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="3d8fc-121">Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="3d8fc-122">Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres, sammen med årsaken til at det ikke kunne tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="3d8fc-123">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="3d8fc-124">Tilbakeføring av bilag fra bilagstransaksjonslisten.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="3d8fc-125">Du kan også tilbakeføre bilag fra **bilagstransaksjonslisten** på tvers av alle underfinansjournaler.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="3d8fc-126">I tillegg kan du tilbakeføre flere enn ett bilag om gangen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="3d8fc-127">Slik tilbakefører du ett eller flere bilag:</span><span class="sxs-lookup"><span data-stu-id="3d8fc-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="3d8fc-128">Velg **Tilbakefør**-menyen øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="3d8fc-129">Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="3d8fc-130">Velg **Ja** hvis du vil bruke de eksisterende transaksjonsdatoene, eller **Nei** hvis du vil angi en ny.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="3d8fc-131">I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket, og du må angi en ny transaksjonsdato for å tilbakeføre den.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="3d8fc-132">Hvis du velger **Nei**, angir du en transaksjonsdato for tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="3d8fc-133">Angi en kommentar for å beskrive tilbakeføringstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="3d8fc-134">Velg **Tilbakeføring**-knappen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="3d8fc-135">Transaksjonen blir tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="3d8fc-136">Hvis det finnes mer enn 100 bilagslinjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="3d8fc-137">Du kan se gjennom resultatene ved å vise kommentarene i den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="3d8fc-138">Alle transaksjoner som ikke kan tilbakeføres, registreres i loggen for den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="3d8fc-139">Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="3d8fc-140">Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres, sammen med årsaken til at det ikke kunne tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="3d8fc-141">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="3d8fc-142">Transaksjoner kan bare tilbakeføres hvis de oppfyller forretningsreglene for tilbakeføring.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="3d8fc-143">Leverandørbetalinger kan ikke reverseres ved hjelp av funksjonen som er beskrevet i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="3d8fc-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="3d8fc-144">Leverandørbetalinger må tilbakeføres ved å følge fremgangsmåten i [Tilbakeføre en leverandørbetaling](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="3d8fc-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]