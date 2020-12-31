---
title: Redusere saldoavskrivning etter en deling
description: Dette emnet beskriver metoden som brukes i anleggsmidler til å beregne avskrivning etter at et aktiva er delt, ved å bruke metoden for reduksjon av saldo.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
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
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 615d17c71b904d426081d4c57492ba7e95c2c749
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650677"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="58451-103">Redusere saldoavskrivning etter en deling</span><span class="sxs-lookup"><span data-stu-id="58451-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58451-104">Dette emnet beskriver metoden som brukes i anleggsmidler til å beregne avskrivning etter at et aktiva er delt til et annet aktiva, ved å bruke metoden for reduksjon av saldo.</span><span class="sxs-lookup"><span data-stu-id="58451-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="58451-105">Avskrivningsåret som er konfigurert i aktivatablået, er regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="58451-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="58451-106">Hvis du vil ha mer informasjon, kan du se [Redusere saldoavskrivning](reduce-balance-depreciation.md) og [Dele et anleggsmiddel](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="58451-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="58451-107">Hvis du deler et anleggsmiddel i løpet av en regnskapsperiode som er senere enn perioden da anleggsmidlet ble anskaffet, vil den reduserte saldoavskrivningen redegjøre for aktivaets netto bokførte verdi for fjoråret.</span><span class="sxs-lookup"><span data-stu-id="58451-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="58451-108">Det vil også ta redegjøre for justeringstransaksjoner for anskaffelse og avskrivning som ble generert fra transaksjonen som delte opp aktivaet.</span><span class="sxs-lookup"><span data-stu-id="58451-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="58451-109">Denne virkemåten forutsetter at aktivaet ble anskaffet i ett regnskapsår og delt i et senere regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="58451-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="58451-110">Beløpet som må avskrives for det opprinnelige aktivaet etter at delingen gjenspeiler aktivaets netto bokførte verdi før aktivaet ble delt, og justeringstransaksjonen for anskaffelse og avskrivning som ble postert for delingen.</span><span class="sxs-lookup"><span data-stu-id="58451-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="58451-111">Følgende betingelser gjelder for eksempel:</span><span class="sxs-lookup"><span data-stu-id="58451-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="58451-112">Regnskapsperioden er fra 30. juni til 1. juli.</span><span class="sxs-lookup"><span data-stu-id="58451-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="58451-113">Saldoverdiprosent er 18 prosent, og et aktiva anskaffes i juni 2019 til en anskaffelsespris på $10.000.</span><span class="sxs-lookup"><span data-stu-id="58451-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="58451-114">Avskrivningen for det første regnskapsåret er lik $18.000, den månedlige avskrivningen er lik $150, og aktivaet blir deretter avskrevet til november 2019 med $738,75.</span><span class="sxs-lookup"><span data-stu-id="58451-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="58451-115">I november 2019 deles 80 prosent av aktivaet med et anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="58451-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="58451-116">[![Redusere saldoavskrivning etter en deling](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="58451-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="58451-117">Beløpet som skal avskrives for det opprinnelige aktivaet, er $1822,25.</span><span class="sxs-lookup"><span data-stu-id="58451-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="58451-118">Dette beløpet er lik netto bokført verdi før delingstransaksjonen posteres ($9 111,25), pluss anskaffelsesjusteringen som genereres under postering av delingstransaksjonen (-$8 000), pluss avskrivningsjusteringen som genereres i løpet av delingstransaksjonen ($711).</span><span class="sxs-lookup"><span data-stu-id="58451-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="58451-119">Derfor er avskrivningen for det andre året (1 822,25 × 18 prosent) ÷ 12 = $27,33.</span><span class="sxs-lookup"><span data-stu-id="58451-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="58451-120">Beløpet som skal avskrives for det nye aktivaet i det første året er (8 000 × 18 prosent) ÷ 12 = $120.</span><span class="sxs-lookup"><span data-stu-id="58451-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>
