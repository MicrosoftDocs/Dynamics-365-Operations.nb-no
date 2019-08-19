---
title: Opprette finansavsetningstransaksjoner
description: Denne oppgaveveiledningen viser trinn for å generere finansavsetningstransaksjoner som er basert på avsetningsplaner.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06743ca3ed13906e3f65d3783db7a7f74fb53e3f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846613"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="c2f62-103">Opprette finansavsetningstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="c2f62-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2f62-104">Denne oppgaveveiledningen viser trinn for å generere finansavsetningstransaksjoner som er basert på avsetningsplaner</span><span class="sxs-lookup"><span data-stu-id="c2f62-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="c2f62-105">Gå til Økonomimodul > Journaloppføringer > Økonomijournaler.</span><span class="sxs-lookup"><span data-stu-id="c2f62-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="c2f62-106">Finn og velg ønsket journal i listen, eller opprett en ny.</span><span class="sxs-lookup"><span data-stu-id="c2f62-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="c2f62-107">Klikk for å følge koblingen i Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2f62-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="c2f62-108">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c2f62-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="c2f62-109">Angi de ønskede verdiene i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2f62-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="c2f62-110">I dette eksemplet definerer vi utgiften for forsikring.</span><span class="sxs-lookup"><span data-stu-id="c2f62-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="c2f62-111">Den blir periodisk utgiftsbeløp.</span><span class="sxs-lookup"><span data-stu-id="c2f62-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="c2f62-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c2f62-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="c2f62-113">Angi et tall i Debet-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2f62-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="c2f62-114">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2f62-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="c2f62-115">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="c2f62-115">Click Functions.</span></span>
10. <span data-ttu-id="c2f62-116">Velg Finansavsetninger.</span><span class="sxs-lookup"><span data-stu-id="c2f62-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="c2f62-117">Klikk rullegardinknappen i feltet Avsetningsidentifikasjon for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c2f62-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="c2f62-118">Finn og velg avsetningsplanen du vil bruke, i listen.</span><span class="sxs-lookup"><span data-stu-id="c2f62-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="c2f62-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c2f62-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c2f62-120">Angi en dato i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2f62-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="c2f62-121">Klikk Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="c2f62-121">Click Transactions.</span></span>
16. <span data-ttu-id="c2f62-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c2f62-122">Close the page.</span></span>
17. <span data-ttu-id="c2f62-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c2f62-123">Click OK.</span></span>
18. <span data-ttu-id="c2f62-124">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="c2f62-124">Click Post.</span></span>

