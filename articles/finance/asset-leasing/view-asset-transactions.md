---
title: Vise gjelds-, aktiva- og utgiftstransaksjoner
description: Dette emnet forklarer hvordan du viser transaksjoner for en leid eiendel. Disse transaksjonene omfatter leieforpliktelsestransaksjoner og fullbyrdelsesutgiftstransaksjoner som er postert.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7008891d194dc990d13a9f56db155c6990aae0c0
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446609"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="120f8-104">Vise gjelds-, aktiva- og utgiftstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="120f8-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="120f8-105">Dette emnet forklarer hvordan du viser transaksjoner for en leid eiendel.</span><span class="sxs-lookup"><span data-stu-id="120f8-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="120f8-106">Disse transaksjonene omfatter leieforpliktelsestransaksjoner og fullbyrdelsesutgiftstransaksjoner som er postert.</span><span class="sxs-lookup"><span data-stu-id="120f8-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="120f8-107">De bærende verdiene for gjeld og bruksrettseiendel brukes i flere rapporter.</span><span class="sxs-lookup"><span data-stu-id="120f8-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="120f8-108">De brukes også til å beregne justeringsverdier.</span><span class="sxs-lookup"><span data-stu-id="120f8-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="120f8-109">Gjeldstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="120f8-109">Liability transactions</span></span>

<span data-ttu-id="120f8-110">Hvis du vil vise leieforpliktelsestransaksjoner, velger du en leieavtale på siden **Leiesammendrag**, og deretter velger du **Tablåer** for å åpne tablåene som er knyttet til leieposten.</span><span class="sxs-lookup"><span data-stu-id="120f8-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="120f8-111">Etter at en opprinnelig gjenkjenning, en faktura eller en rentejournal er postert, velger du **Gjeldstransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="120f8-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="120f8-112">Siden **Gjeldstransaksjoner** viser transaksjonene som enten øker eller reduserer leieforpliktelsen.</span><span class="sxs-lookup"><span data-stu-id="120f8-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="120f8-113">Negative beløp på denne siden representerer kredittransaksjoner i standardprogrammet.</span><span class="sxs-lookup"><span data-stu-id="120f8-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="120f8-114">Eventuelle renteavsetninger vises som negative verdier, og øker de totale leieforpliktelsene.</span><span class="sxs-lookup"><span data-stu-id="120f8-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="120f8-115">Eventuelle leiejusteringer vises som positive eller negative verdier, avhengig av leietablåets natur og virkning.</span><span class="sxs-lookup"><span data-stu-id="120f8-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="120f8-116">Gjeldende nettototalsaldo for leieforpliktelsen for den valgte leien vises nederst til venstre på siden.</span><span class="sxs-lookup"><span data-stu-id="120f8-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="120f8-117">Aktivatransaksjoner</span><span class="sxs-lookup"><span data-stu-id="120f8-117">Asset transactions</span></span>

<span data-ttu-id="120f8-118">Hvis du vil vise leieaktivatransaksjoner, velger du en leieavtale på siden **Leiesammendrag**, og deretter velger du **Tablåer** for å åpne leietablåene som er knyttet til leieposten.</span><span class="sxs-lookup"><span data-stu-id="120f8-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="120f8-119">Velg deretter **Leietransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="120f8-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="120f8-120">Siden **Aktivatransaksjon** viser transaksjonene som enten øker eller reduserer leieaktivaet og akkumulerte avskrivningskontoer.</span><span class="sxs-lookup"><span data-stu-id="120f8-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="120f8-121">Debet vises som positive verdier, og kredit vises som negative verdier, som på **Gjeldstransaksjoner**-siden.</span><span class="sxs-lookup"><span data-stu-id="120f8-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="120f8-122">Den posterte opprinnelige gjenkjenningen og den neste akkumulerte avskrivningen vises nederst til venstre på siden som anleggsmiddelsaldoen.</span><span class="sxs-lookup"><span data-stu-id="120f8-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="120f8-123">Utgiftstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="120f8-123">Expenses transactions</span></span>

<span data-ttu-id="120f8-124">Hvis du vil vise leieutgiftstransaksjoner, velger du en leieavtale på siden **Leiesammendrag**, og deretter velger du **Tablåer** for å åpne leietablåene som er knyttet til leieposten.</span><span class="sxs-lookup"><span data-stu-id="120f8-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="120f8-125">Deretter velger du **Utgiftstransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="120f8-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="120f8-126">Siden **Utgiftstransaksjoner** viser alle utgifter som er postert mot leieavtalen, for eksempel renteutgifter, avskrivningsutgifter og eventuelle fullbyrdelseskostnader.</span><span class="sxs-lookup"><span data-stu-id="120f8-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>
