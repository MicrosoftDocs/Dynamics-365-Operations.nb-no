---
title: Balanserte journaler for interenhetsregnskap
description: Denne artikkelen viser hvordan en journal belastes automatisk når en balanserende finansdimensjon er valgt på Finans-siden.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b596a2332a9ada01df7b4e718a79eb624ee52fc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "326774"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="9d43e-103">Balanserte journaler for interenhetsregnskap</span><span class="sxs-lookup"><span data-stu-id="9d43e-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d43e-104">Denne artikkelen viser hvordan en journal belastes automatisk når en balanserende finansdimensjon er valgt på Finans-siden.</span><span class="sxs-lookup"><span data-stu-id="9d43e-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="9d43e-105">Hvis kontooppføringer ikke balanseres på nivået for verdiene for finansdimensjonen, blir det automatisk opprettet tilleggskontooppføringer for å balansere journalen.</span><span class="sxs-lookup"><span data-stu-id="9d43e-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="9d43e-106">Disse kontooppføringene bruker posteringstypene **Enhetsintern - debet**og **Enhetsintern - kredit** på siden **Kontoer for automatiske transaksjoner** for å bestemme hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="9d43e-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="9d43e-107">For eksempel Forretningsenhet, som er det andre segmentet i finanskontoen, er valgt som den balanserende finansdimensjonen, og følgende regnskapsoppføringer skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="9d43e-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="9d43e-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="9d43e-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="9d43e-109">100,00 D</span><span class="sxs-lookup"><span data-stu-id="9d43e-109">100.00 DR</span></span> |
| <span data-ttu-id="9d43e-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="9d43e-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="9d43e-111">100,00 D</span><span class="sxs-lookup"><span data-stu-id="9d43e-111">100.00 DR</span></span> |
| <span data-ttu-id="9d43e-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="9d43e-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="9d43e-113">200,00 K</span><span class="sxs-lookup"><span data-stu-id="9d43e-113">200.00 CR</span></span> |

<span data-ttu-id="9d43e-114">I dette tilfellet bestemmes følgende saldoer: </span><span class="sxs-lookup"><span data-stu-id="9d43e-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="9d43e-115">For Forretningsenhet MSP = 100,00 K</span><span class="sxs-lookup"><span data-stu-id="9d43e-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="9d43e-116">For Forretningsenhet NY = 100,00 D</span><span class="sxs-lookup"><span data-stu-id="9d43e-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="9d43e-117">Følgende regnskapsoppføringer opprettes derfor automatisk for å balansere journalen på nivået til finansdimensjonsverdiene.</span><span class="sxs-lookup"><span data-stu-id="9d43e-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="9d43e-118">(Enhetsintern debet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="9d43e-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="9d43e-119">100,00 D</span><span class="sxs-lookup"><span data-stu-id="9d43e-119">100.00 DR</span></span> |
| <span data-ttu-id="9d43e-120">(Enhetsintern kredit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="9d43e-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="9d43e-121">100,00 K</span><span class="sxs-lookup"><span data-stu-id="9d43e-121">100.00 CR</span></span> |





