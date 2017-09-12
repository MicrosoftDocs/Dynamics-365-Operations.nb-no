---
title: "Avledede tablåer"
description: "Denne artikkelen inneholder en oversikt over den avledede tablåfunksjonaliteten."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5afdabf93128bc52cb223d0c35c6bcdae5f5ca2a
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

# <a name="derived-books"></a><span data-ttu-id="37999-103">Avledede tablåer</span><span class="sxs-lookup"><span data-stu-id="37999-103">Derived books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="37999-104">Denne artikkelen inneholder en oversikt over den avledede tablåfunksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="37999-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="37999-105">Formålet med avledede tablåer er å forenkle postering av anleggsmiddeltablåtransaksjoner som er planlagt for regelmessige intervaller.</span><span class="sxs-lookup"><span data-stu-id="37999-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="37999-106">Du kan velge ett tablå som det primære tablået.</span><span class="sxs-lookup"><span data-stu-id="37999-106">You choose one book as the primary book.</span></span> <span data-ttu-id="37999-107">Dette er vanligvis tablået som brukes til regnskapsavskrivning.</span><span class="sxs-lookup"><span data-stu-id="37999-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="37999-108">Du knytter det deretter til de andre tablåene som brukes til å postere transaksjoner i samme intervaller som det primære tablået.</span><span class="sxs-lookup"><span data-stu-id="37999-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="37999-109">Tablåer for avskrivning av skatt brukes ofte som avledede tablåer.</span><span class="sxs-lookup"><span data-stu-id="37999-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="37999-110">De vanligste transaksjonene som brukes til å postere til avledede tablåer, er anskaffelse, anskaffelsesjusteringer og anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="37999-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="37999-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="37999-111">Example</span></span>

<span data-ttu-id="37999-112">Tablå B og tablå C er satt opp som avledede tablåer for tablå A for anskaffelsestransaksjonstypen.</span><span class="sxs-lookup"><span data-stu-id="37999-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="37999-113">I tablå A oppgir du en anskaffelsestransaksjon på 1500,00 for anleggsmiddel 123.</span><span class="sxs-lookup"><span data-stu-id="37999-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="37999-114">Når transaksjonen er postert, genereres en anskaffelsestransaksjon på 1500,00 som posteres for anleggsmiddel 123 i tablå B, og for anleggsmiddel 123 i tablå C.</span><span class="sxs-lookup"><span data-stu-id="37999-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="37999-115">Når du forbereder transaksjonene for det primære tablået som skal posteres i anleggsmiddeljournalen, kan du også vise og endre transaksjonene til de avledede tablåene.</span><span class="sxs-lookup"><span data-stu-id="37999-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="37999-116">Hvis du forbereder de primære tablåtransaksjonene i en annen journal, vises ikke transaksjonene til den avledede verdien.</span><span class="sxs-lookup"><span data-stu-id="37999-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="37999-117">De posteres imidlertid til de passende kontoene og posteringslagene når du posterer de primære tablåtransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="37999-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="37999-118">Tablåer som brukes til å postere transaksjoner i intervaller som er forskjellig fra intervallene til det primære tablået, må knyttes til de faste anleggsmidlene som separate tablåer, og ikke som avledede tablåer.</span><span class="sxs-lookup"><span data-stu-id="37999-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="37999-119">Hvis du vil ha mer informasjon, kan du se [Postere med avledede tablåer](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="37999-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>




