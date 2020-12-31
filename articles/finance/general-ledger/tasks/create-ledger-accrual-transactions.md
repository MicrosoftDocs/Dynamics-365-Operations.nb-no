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
ms.openlocfilehash: 2112336045086d0eb3b2fb0018f33631528a05ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446300"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="6026a-103">Opprette finansavsetningstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="6026a-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6026a-104">Denne oppgaveveiledningen viser trinn for å generere finansavsetningstransaksjoner som er basert på avsetningsplaner</span><span class="sxs-lookup"><span data-stu-id="6026a-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="6026a-105">Gå til Økonomimodul > Journaloppføringer > Økonomijournaler.</span><span class="sxs-lookup"><span data-stu-id="6026a-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="6026a-106">Finn og velg ønsket journal i listen, eller opprett en ny.</span><span class="sxs-lookup"><span data-stu-id="6026a-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="6026a-107">Klikk for å følge koblingen i Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="6026a-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="6026a-108">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6026a-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="6026a-109">Angi de ønskede verdiene i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="6026a-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="6026a-110">I dette eksemplet definerer vi utgiften for forsikring.</span><span class="sxs-lookup"><span data-stu-id="6026a-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="6026a-111">Den blir periodisk utgiftsbeløp.</span><span class="sxs-lookup"><span data-stu-id="6026a-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="6026a-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6026a-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="6026a-113">Angi et tall i Debet-feltet.</span><span class="sxs-lookup"><span data-stu-id="6026a-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="6026a-114">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="6026a-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="6026a-115">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="6026a-115">Click Functions.</span></span>
10. <span data-ttu-id="6026a-116">Velg Finansavsetninger.</span><span class="sxs-lookup"><span data-stu-id="6026a-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="6026a-117">Klikk rullegardinknappen i feltet Avsetningsidentifikasjon for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6026a-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="6026a-118">Finn og velg avsetningsplanen du vil bruke, i listen.</span><span class="sxs-lookup"><span data-stu-id="6026a-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="6026a-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6026a-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6026a-120">Angi en dato i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="6026a-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="6026a-121">Klikk Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="6026a-121">Click Transactions.</span></span>
16. <span data-ttu-id="6026a-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6026a-122">Close the page.</span></span>
17. <span data-ttu-id="6026a-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6026a-123">Click OK.</span></span>
18. <span data-ttu-id="6026a-124">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="6026a-124">Click Post.</span></span>

