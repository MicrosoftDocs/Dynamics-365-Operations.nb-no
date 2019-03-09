---
title: Avskrivning av anleggsmidler
description: Dette emnet gir en oversikt over avskrivning for anleggsmidler.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a82e14e12cbde29e5619518481d0c22f6fa1a37a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "332800"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="cbf8e-103">Avskrivning av anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="cbf8e-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cbf8e-104">Dette emnet gir en oversikt over avskrivning for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="cbf8e-105">Avskrivning er en periodisk transaksjon som vanligvis reduserer verdien til anleggsmidlene i balansen, og kostnadsføres som en utgift i en resultatkonto.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="cbf8e-106">Derfor brukes vanligvis en hovedkonto til å kreditere den periodiske avskrivningen i balansen.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="cbf8e-107">En motkonto er en konto i resultatdelen av kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="cbf8e-108">Avskrivningsjustering</span><span class="sxs-lookup"><span data-stu-id="cbf8e-108">Depreciation adjustment</span></span>
<span data-ttu-id="cbf8e-109">Vanligvis posteres kun en korrigering til en postert avskrivningstransaksjon som en avskrivningsjustering.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="cbf8e-110">Derfor konfigureres både hovedkontoen og motkontoen på samme måte som avskrivningskontoen.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="cbf8e-111">En avskrivningsjustering kan være et positivt eller negativt beløp, men funksjonaliteten for hovedkontoen (som en balansekonto) og motkontoen (vanligvis som en resultatkonto) er den samme.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="cbf8e-112">Ekstraordinær avskrivning</span><span class="sxs-lookup"><span data-stu-id="cbf8e-112">Extraordinary depreciation</span></span>
<span data-ttu-id="cbf8e-113">Ekstraordinær avskrivning fungerer som grunnleggende avskrivning.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="cbf8e-114">Derfor brukes en hovedkonto til å kreditere avskrivningsbeløpet i balansen og redusere verdien til anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="cbf8e-115">En motkonto er en resultatkonto, der avskrivningen som beregnes for regnskapsperioden, kostnadsføres som en utgift.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="cbf8e-116">Ekstraordinær avskrivning fungerer uavhengig av grunnleggende avskrivning.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="cbf8e-117">Når du har ekstraordinær avskrivning som en separat transaksjonstype, kan du postere og rapportere den ekstraordinære avskrivningen separat fra den vanlige, grunnleggende avskrivningen.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="cbf8e-118">Særskilte avskrivningsfradrag</span><span class="sxs-lookup"><span data-stu-id="cbf8e-118">Special depreciation allowance</span></span>
<span data-ttu-id="cbf8e-119">Du kan bruke særskilte avskrivningsfradrag til å ta ekstra avskrivningsbeløp første året et anleggsmiddel settes i drift og avskrives.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="cbf8e-120">Særskilte avskrivningsfradrag må utføres før alle andre avskrivningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="cbf8e-121">Fordi særskilte avskrivningsfradrag ofte er ukjente før senere i levetiden for anleggsmidlet, er det best å bruke denne typen avskrivning i et tablå som ikke posteres til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="cbf8e-122">Du kan bruke funksjonen Slett transaksjoner som ikke er postert til økonomimodulen, til å slette transaksjonsloggen for disse tablåene.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="cbf8e-123">Du kan deretter slette avskrivningsloggen for anleggsmiddeltablået, postere det særskilte avskrivningsfradraget når det er kjent, og deretter postere de gjenværende avskrivningstransaksjonene for året.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="cbf8e-124">Du kan opprette et ubegrenset antall poster for særskilte avskrivningsfradrag.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="cbf8e-125">Når du har tildelt disse postene til et tablå for anleggsmiddelgruppe, brukes de for anleggsmiddeltablået.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="cbf8e-126">Et særskilt avskrivningsfradrag angis som en prosent eller et fast beløp.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="cbf8e-127">Når du posterer avskrivningsforslag, posteres transaksjoner med særskilte avskrivningsfradrag til tablået som transaksjoner som er separate fra avskrivningstransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="cbf8e-128"> Avskrivningskalendere</span><span class="sxs-lookup"><span data-stu-id="cbf8e-128">Depreciation calendars</span></span>
<span data-ttu-id="cbf8e-129">Hvert tablå inneholder en kalender som skal brukes ved avskrivning av anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="cbf8e-130">Tablået bruker regnskapskalenderen for finans som standard hvis du ikke angir en kalender for tablået.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="cbf8e-131">Du må velge en regnskapskalender for et tablå når avskrivningsprofilen som er knyttet til tablået, bruker et avskrivningsår.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="cbf8e-132">Du kan opprette delte kalendere ved hjelp av siden **Økonomiske kalendere** i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="cbf8e-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="cbf8e-133">Hvis du vil ha mer informasjon, kan du se [Avskrivningsmetoder og -konvensjoner](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="cbf8e-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>



