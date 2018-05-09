--- 
title: Definer mva-koder
description: "Mva-koder opprettes for hver indirekte merverdiavgift eller annen avgift som den juridiske enheten er forpliktet til å beregne, samle inn og betale til skattemyndighetene."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 20033cef966a643b7735d488bc354136dc55d6b0
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="5d410-103">Definer mva-koder</span><span class="sxs-lookup"><span data-stu-id="5d410-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d410-104">Mva-koder opprettes for hver indirekte merverdiavgift eller annen avgift som den juridiske enheten er forpliktet til å beregne, samle inn og betale til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="5d410-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="5d410-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="5d410-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="5d410-106">Gå til Avgift > Indirekte avgifter > Merverdiavgift > Mva-koder.</span><span class="sxs-lookup"><span data-stu-id="5d410-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="5d410-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5d410-107">Click New.</span></span>
3. <span data-ttu-id="5d410-108">Skriv inn en verdi i Mva-kode-feltet.</span><span class="sxs-lookup"><span data-stu-id="5d410-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="5d410-109">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5d410-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5d410-110">Velg en utligningsperiode for å angi hvilken skattemyndighet og i hvilke intervaller denne merverdiavgiften må rapporteres og betales.</span><span class="sxs-lookup"><span data-stu-id="5d410-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="5d410-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5d410-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5d410-112">Velg en finansposteringsgruppe for å angi hovedkontoene for å postere merverdiavgift til økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="5d410-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="5d410-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5d410-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="5d410-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5d410-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="5d410-115">Vis hurtigfanen Beregning.</span><span class="sxs-lookup"><span data-stu-id="5d410-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="5d410-116">Hurtigfanen Beregning inneholder flere felt som kontrollerer hvordan mva-beløp skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="5d410-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="5d410-117">Klikk Mva-kode i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5d410-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="5d410-118">Velg Verdier.</span><span class="sxs-lookup"><span data-stu-id="5d410-118">Click Values.</span></span>
13. <span data-ttu-id="5d410-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5d410-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="5d410-120">Angi verdien for denne mva-koden.</span><span class="sxs-lookup"><span data-stu-id="5d410-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="5d410-121">Hvis Beløp per enhet er valg i hurtigfanen Beregning i Opprinnelse-feltet, ganges verdien med antallet på transaksjonen for å beregne mva-beløpet.</span><span class="sxs-lookup"><span data-stu-id="5d410-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="5d410-122">Hvis mva-koden ikke er en enhetsbasert avgift, er verdien en prosent som er brukt på opprinnelsen for denne mva-koden for å beregne mva-beløpet.</span><span class="sxs-lookup"><span data-stu-id="5d410-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="5d410-123">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5d410-123">Click Save.</span></span>
16. <span data-ttu-id="5d410-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5d410-124">Close the page.</span></span>
17. <span data-ttu-id="5d410-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5d410-125">Click Save.</span></span>


