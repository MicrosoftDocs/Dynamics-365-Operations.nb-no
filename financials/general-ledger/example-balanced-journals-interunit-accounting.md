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
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: nb-no
ms.lasthandoff: 06/29/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="43187-103">Balanserte journaler for interenhetsregnskap</span><span class="sxs-lookup"><span data-stu-id="43187-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="43187-104">Denne artikkelen viser hvordan en journal belastes automatisk når en balanserende finansdimensjon er valgt på Finans-siden.</span><span class="sxs-lookup"><span data-stu-id="43187-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="43187-105">Hvis kontooppføringer ikke balanseres på nivået for verdiene for finansdimensjonen, blir det automatisk opprettet tilleggskontooppføringer for å balansere journalen.</span><span class="sxs-lookup"><span data-stu-id="43187-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="43187-106">Disse kontooppføringene bruker posteringstypene **Enhetsintern - debet**og **Enhetsintern - kredit** på siden **Kontoer for automatiske transaksjoner** for å bestemme hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="43187-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="43187-107">For eksempel avdeling, som er det andre segmentet i finanskontoen, er valgt som den balanserende finansdimensjonen, og følgende regnskapsoppføringer skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="43187-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="43187-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="43187-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="43187-109">100,00 D</span><span class="sxs-lookup"><span data-stu-id="43187-109">100.00 DR</span></span> |
| <span data-ttu-id="43187-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="43187-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="43187-111">100,00 D</span><span class="sxs-lookup"><span data-stu-id="43187-111">100.00 DR</span></span> |
| <span data-ttu-id="43187-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="43187-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="43187-113">200,00 K</span><span class="sxs-lookup"><span data-stu-id="43187-113">200.00 CR</span></span> |

<span data-ttu-id="43187-114">I dette tilfellet bestemmes følgende saldoer: </span><span class="sxs-lookup"><span data-stu-id="43187-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="43187-115">For avdeling MSP = 100,00 K</span><span class="sxs-lookup"><span data-stu-id="43187-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="43187-116">For avdeling NY = 100,00 K</span><span class="sxs-lookup"><span data-stu-id="43187-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="43187-117">Følgende regnskapsoppføringer opprettes derfor automatisk for å balansere journalen på nivået til finansdimensjonsverdiene.</span><span class="sxs-lookup"><span data-stu-id="43187-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="43187-118">(Enhetsintern debet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="43187-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="43187-119">100,00 D</span><span class="sxs-lookup"><span data-stu-id="43187-119">100.00 DR</span></span> |
| <span data-ttu-id="43187-120">(Enhetsintern kredit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="43187-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="43187-121">100,00 K</span><span class="sxs-lookup"><span data-stu-id="43187-121">100.00 CR</span></span> |






