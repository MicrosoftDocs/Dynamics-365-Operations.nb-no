---
title: Definer mva-koder
description: Dette emnet forklarer hvordan du definerer merverdiavgiftskoder i Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3dad006b486f7cd6714c713a3bd83a95fdf0d2b5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979644"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="cec8f-103">Definer mva-koder</span><span class="sxs-lookup"><span data-stu-id="cec8f-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cec8f-104">Dette emnet forklarer hvordan du definerer merverdiavgiftskoder.</span><span class="sxs-lookup"><span data-stu-id="cec8f-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="cec8f-105">Mva-koder opprettes for hver indirekte merverdiavgift eller annen avgift som den juridiske enheten er forpliktet til å beregne, samle inn og betale til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="cec8f-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="cec8f-106">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="cec8f-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="cec8f-107">Gå til **Navigasjonsrute > Avgift > Indirekte avgifter > Merverdiavgift > Mva-koder** .</span><span class="sxs-lookup"><span data-stu-id="cec8f-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes** .</span></span>
2. <span data-ttu-id="cec8f-108">Velg **Ny** .</span><span class="sxs-lookup"><span data-stu-id="cec8f-108">Select **New** .</span></span>
3. <span data-ttu-id="cec8f-109">Skriv inn en verdi i **Mva-kode** -feltet.</span><span class="sxs-lookup"><span data-stu-id="cec8f-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="cec8f-110">Skriv inn en verdi i **Navn** -feltet.</span><span class="sxs-lookup"><span data-stu-id="cec8f-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="cec8f-111">Velg en **utligningsperiode** ved å åpne rullegardinlisten for å angi hvilken skattemyndighet og i hvilke intervaller denne merverdiavgiften må rapporteres og betales.</span><span class="sxs-lookup"><span data-stu-id="cec8f-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="cec8f-112">Velg en **finansposteringsgruppe** for å angi hovedkontoene for å postere merverdiavgift til økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="cec8f-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="cec8f-113">Vis hurtigfanen **Beregning** .</span><span class="sxs-lookup"><span data-stu-id="cec8f-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="cec8f-114">Den inneholder flere felt som kontrollerer hvordan mva-beløp skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="cec8f-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="cec8f-115">Fyll ut disse feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="cec8f-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="cec8f-116">I **handlingsruten** øverst i grensesnittet velger du **Mva-kode** .</span><span class="sxs-lookup"><span data-stu-id="cec8f-116">On the **Action Pane** at the top of the interface, select **Sales tax code** .</span></span>
9. <span data-ttu-id="cec8f-117">Velg **Verdier** .</span><span class="sxs-lookup"><span data-stu-id="cec8f-117">Select **Values** .</span></span>
10. <span data-ttu-id="cec8f-118">Angi verdien for denne mva-koden i **Verdi** -kolonnen.</span><span class="sxs-lookup"><span data-stu-id="cec8f-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="cec8f-119">Hvis Beløp per enhet er valg i hurtigfanen **Beregning** i Opprinnelse-feltet, ganges verdien med antallet på transaksjonen for å beregne mva-beløpet.</span><span class="sxs-lookup"><span data-stu-id="cec8f-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="cec8f-120">Hvis mva-koden ikke er en enhetsbasert avgift, er verdien en prosent som er brukt på opprinnelsen for denne mva-koden for å beregne mva-beløpet.</span><span class="sxs-lookup"><span data-stu-id="cec8f-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="cec8f-121">Velg **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="cec8f-121">Select **Save** .</span></span>
12. <span data-ttu-id="cec8f-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cec8f-122">Close the page.</span></span>
13. <span data-ttu-id="cec8f-123">Velg **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="cec8f-123">Select **Save** .</span></span>

