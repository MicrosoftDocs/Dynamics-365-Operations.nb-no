---
title: Du kan ikke fakturere en kunderettet salgsordre
description: Du kan ikke lenger fakturere den opprinnelige salgsordren og den opprinnelige direkteleveringsbestillingen etter at du har aktivert alternativet Poster faktura automatisk.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026775"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="2f1b1-103">Du kan ikke fakturere en kunderettet salgsordre</span><span class="sxs-lookup"><span data-stu-id="2f1b1-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="2f1b1-104">KB-nummer: 4611793</span><span class="sxs-lookup"><span data-stu-id="2f1b1-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="2f1b1-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="2f1b1-105">Symptoms</span></span>

<span data-ttu-id="2f1b1-106">Du kan ikke lenger fakturere den opprinnelige salgsordren og den opprinnelige direkteleveringsbestillingen etter at du har aktivert alternativet **Poster faktura automatisk** på siden **Konsernintern** for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="2f1b1-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="2f1b1-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="2f1b1-107">Resolution</span></span>

<span data-ttu-id="2f1b1-108">Synkroniseringsvirkemåten for konserninterne fakturaer og fakturaer for direkteleveringsordrer styres og tvinges av parameterne som er beskrevet i [Definere parametere for å postere en konsernintern ordre](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span><span class="sxs-lookup"><span data-stu-id="2f1b1-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="2f1b1-109">Når du har definert disse parameterne, må du fakturere den konserninterne salgsordren først.</span><span class="sxs-lookup"><span data-stu-id="2f1b1-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="2f1b1-110">De opprinnelige salgsordrene og bestillingene vil deretter synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="2f1b1-110">The original sales orders and purchase orders will then be synchronized.</span></span>
