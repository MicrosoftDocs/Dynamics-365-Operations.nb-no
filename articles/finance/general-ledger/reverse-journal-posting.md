---
title: Tilbakeføre journalpostering
description: Dette emnet beskriver funksjoner som lar deg tilbakeføre bilag fra bilagstransaksjonslisten eller fra finansjournaler.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248591"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="1a0b9-103">Tilbakeføre journalpostering</span><span class="sxs-lookup"><span data-stu-id="1a0b9-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a0b9-104">Dette emnet beskriver funksjonene i Microsoft Dynamics 365 Finance som lar deg tilbakeføre en hel journal eller tilbakeføre ett eller flere bilag fra bilagstransaksjonslisten, uavhengig av opprinnelsen.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="1a0b9-105">Tilbakeføre journaler</span><span class="sxs-lookup"><span data-stu-id="1a0b9-105">Reversing journals</span></span>

<span data-ttu-id="1a0b9-106">Du kan tilbakeføre Journallinjer enkeltvis.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="1a0b9-107">Med tilbakeføring av journalpostering kan du også tilbakeføre en hel finansjournal.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="1a0b9-108">Slik tilbakefører du en journal:</span><span class="sxs-lookup"><span data-stu-id="1a0b9-108">To reverse a journal:</span></span> 
- <span data-ttu-id="1a0b9-109">Åpne finansjournalen, og filtrer på posterte journaler</span><span class="sxs-lookup"><span data-stu-id="1a0b9-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="1a0b9-110">Klikk på Tilbakefør-menyen øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="1a0b9-111">Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført</span><span class="sxs-lookup"><span data-stu-id="1a0b9-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="1a0b9-112">Velg Ja hvis du vil bruke de eksisterende transaksjonsdatoene, eller Nei hvis du vil angi en ny.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="1a0b9-113">I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket og du vil angi en ny transaksjonsdato for tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="1a0b9-114">Hvis du valgte Nei, angir du en transaksjonsdato for tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="1a0b9-115">Angi en kommentar som du vil legge til i tilbakeføringstransaksjonen</span><span class="sxs-lookup"><span data-stu-id="1a0b9-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="1a0b9-116">Klikk på Tilbakefør-knappen</span><span class="sxs-lookup"><span data-stu-id="1a0b9-116">Click the Reverse button</span></span>

<span data-ttu-id="1a0b9-117">Transaksjonen blir tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="1a0b9-118">Hvis antallet bilagslinjer overskrider 100 linjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="1a0b9-119">Du kan se gjennom resultatene av tilbakeføringen ved å vise kommentarene i den satsvise jobben som ble kjørt.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="1a0b9-120">Alle feil vil bli registrert i loggen for den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="1a0b9-121">Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="1a0b9-122">Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres og årsaken til at det ikke kunne tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="1a0b9-123">Klikk på OK for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="1a0b9-124">Tilbakeføring av bilag fra bilagstransaksjonslisten.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="1a0b9-125">Du kan også tilbakeføre bilag fra **bilagstransaksjonslisten** på tvers av alle underfinansjournaler.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="1a0b9-126">I tillegg kan du tilbakeføre flere enn ett bilag om gangen.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="1a0b9-127">Slik tilbakefører du ett eller flere bilag:</span><span class="sxs-lookup"><span data-stu-id="1a0b9-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="1a0b9-128">Klikk på Tilbakefør-menyen øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="1a0b9-129">Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført</span><span class="sxs-lookup"><span data-stu-id="1a0b9-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="1a0b9-130">Velg Ja hvis du vil bruke de eksisterende transaksjonsdatoene, eller Nei hvis du vil angi en ny.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="1a0b9-131">I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket og du vil angi en ny transaksjonsdato for tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="1a0b9-132">Hvis du valgte Nei, angir du en transaksjonsdato for tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="1a0b9-133">Angi en kommentar som du vil legge til i tilbakeføringstransaksjonen</span><span class="sxs-lookup"><span data-stu-id="1a0b9-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="1a0b9-134">Klikk på Tilbakefør-knappen</span><span class="sxs-lookup"><span data-stu-id="1a0b9-134">Click the Reverse button</span></span>

<span data-ttu-id="1a0b9-135">Transaksjonen blir tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="1a0b9-136">Hvis antallet bilagslinjer overskrider 100 linjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="1a0b9-137">Du kan se gjennom resultatene av tilbakeføringen ved å vise kommentarene i den satsvise jobben som ble kjørt.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="1a0b9-138">Alle feil vil bli registrert i loggen for den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="1a0b9-139">Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="1a0b9-140">Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres og årsaken til at det ikke kunne tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="1a0b9-141">Klikk på OK for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="1a0b9-141">Click on Ok to close the dialog.</span></span>

