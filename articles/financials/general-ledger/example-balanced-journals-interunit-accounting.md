---
title: Balanserte journaler for interenhetsregnskap
description: "Denne artikkelen viser hvordan en journal belastes automatisk når en balanserende finansdimensjon er valgt på Finans-siden."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="6be07-103">Balanserte journaler for interenhetsregnskap</span><span class="sxs-lookup"><span data-stu-id="6be07-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6be07-104">Denne artikkelen viser hvordan en journal belastes automatisk når en balanserende finansdimensjon er valgt på Finans-siden.</span><span class="sxs-lookup"><span data-stu-id="6be07-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="6be07-105">Hvis kontooppføringer ikke balanseres på nivået for verdiene for finansdimensjonen, blir det automatisk opprettet tilleggskontooppføringer for å balansere journalen.</span><span class="sxs-lookup"><span data-stu-id="6be07-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="6be07-106">Disse kontooppføringene bruker posteringstypene **Enhetsintern - debet**og **Enhetsintern - kredit** på siden **Kontoer for automatiske transaksjoner** for å bestemme hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="6be07-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="6be07-107">For eksempel avdeling, som er det andre segmentet i finanskontoen, er valgt som den balanserende finansdimensjonen, og følgende regnskapsoppføringer skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="6be07-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="6be07-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="6be07-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="6be07-109">100,00 D</span><span class="sxs-lookup"><span data-stu-id="6be07-109">100.00 DR</span></span> |
| <span data-ttu-id="6be07-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="6be07-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="6be07-111">100,00 D</span><span class="sxs-lookup"><span data-stu-id="6be07-111">100.00 DR</span></span> |
| <span data-ttu-id="6be07-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="6be07-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="6be07-113">200,00 K</span><span class="sxs-lookup"><span data-stu-id="6be07-113">200.00 CR</span></span> |

<span data-ttu-id="6be07-114">I dette tilfellet bestemmes følgende saldoer: </span><span class="sxs-lookup"><span data-stu-id="6be07-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="6be07-115">For avdeling MSP = 100,00 K</span><span class="sxs-lookup"><span data-stu-id="6be07-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="6be07-116">For avdeling NY = 100,00 K</span><span class="sxs-lookup"><span data-stu-id="6be07-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="6be07-117">Følgende regnskapsoppføringer opprettes derfor automatisk for å balansere journalen på nivået til finansdimensjonsverdiene.</span><span class="sxs-lookup"><span data-stu-id="6be07-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="6be07-118">(Enhetsintern debet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="6be07-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="6be07-119">100,00 D</span><span class="sxs-lookup"><span data-stu-id="6be07-119">100.00 DR</span></span> |
| <span data-ttu-id="6be07-120">(Enhetsintern kredit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="6be07-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="6be07-121">100,00 K</span><span class="sxs-lookup"><span data-stu-id="6be07-121">100.00 CR</span></span> |






