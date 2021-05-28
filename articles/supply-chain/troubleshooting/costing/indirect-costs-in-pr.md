---
title: Rapporten om Indirekte kostnader i prosess omfatter slettede produksjonsordrer
description: Rapporten Indirekte kostnader i prosess presenterer informasjon om produksjonsordrer som ble delvis behandlet og senere slettet.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026780"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="c92ac-103">Rapporten om Indirekte kostnader i prosess omfatter slettede produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="c92ac-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="c92ac-104">KB-nummer: 4612748</span><span class="sxs-lookup"><span data-stu-id="c92ac-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="c92ac-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="c92ac-105">Symptoms</span></span>

<span data-ttu-id="c92ac-106">Rapporten **Indirekte kostnader i prosess** presenterer informasjon om produksjonsordrer som ble delvis behandlet og senere slettet.</span><span class="sxs-lookup"><span data-stu-id="c92ac-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="c92ac-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="c92ac-107">Resolution</span></span>

<span data-ttu-id="c92ac-108">Når du tilbakefører en produksjonsordre, tilbakeføres også alle transaksjonene for denne produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="c92ac-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="c92ac-109">Når du sletter produksjonsordren, fastholder underfinanstabellene og økonomimodulen alle transaksjoner som er tilknyttet den.</span><span class="sxs-lookup"><span data-stu-id="c92ac-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="c92ac-110">Rapportene vil vise transaksjonene i underfinanstabellene.</span><span class="sxs-lookup"><span data-stu-id="c92ac-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="c92ac-111">For den angitte produksjonsordren bør nettoverdien være 0,00.</span><span class="sxs-lookup"><span data-stu-id="c92ac-111">For the specific production order, the net value should be 0.00.</span></span>
