---
title: Feilsøk produktkonfiguratoren
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med produktkonfiguratoren.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d17d9f16f01a68da724751273b7d137a0f0f14de
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248769"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="b4f1f-103">Feilsøk produktkonfiguratoren</span><span class="sxs-lookup"><span data-stu-id="b4f1f-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="b4f1f-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med produktkonfiguratoren.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="b4f1f-105">Vareteksten overskrives når jeg konfigurerer et produkt på en salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b4f1f-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b4f1f-106">Issue description</span></span>

<span data-ttu-id="b4f1f-107">Dette problemet oppstår når du oppretter en salgsordrelinje for en konfigurerbar vare og deretter endrer vareteksten.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="b4f1f-108">Når du konfigurerer varen og deretter velger **OK**, overskrives teksten med standardteksten.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b4f1f-109">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b4f1f-109">Issue resolution</span></span>

<span data-ttu-id="b4f1f-110">Denne virkemåten er forventet.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-110">This behavior is expected.</span></span> <span data-ttu-id="b4f1f-111">Tekstfeltet inneholder variantnavnet, som bare fylles ut etter at du har konfigurert linjen.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="b4f1f-112">Du må derfor endre teksten etter at du har konfigurert linjen, ikke før.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="b4f1f-113">Heltallattributter blir avrundet feil når produktkonfigurasjonsmodeller beregnes.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b4f1f-114">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b4f1f-114">Issue description</span></span>

<span data-ttu-id="b4f1f-115">Dette problemet kan oppstå når du utfører følgende serie med handlinger:</span><span class="sxs-lookup"><span data-stu-id="b4f1f-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="b4f1f-116">Definer følgende attributter i en produksjonskonfigurasjonsmodell:</span><span class="sxs-lookup"><span data-stu-id="b4f1f-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="b4f1f-117">Inndata (heltall)</span><span class="sxs-lookup"><span data-stu-id="b4f1f-117">Input (integer)</span></span>
    - <span data-ttu-id="b4f1f-118">Prosent (desimal)</span><span class="sxs-lookup"><span data-stu-id="b4f1f-118">Percent (decimal)</span></span>
    - <span data-ttu-id="b4f1f-119">Resultat (heltall)</span><span class="sxs-lookup"><span data-stu-id="b4f1f-119">Result (integer)</span></span>

2. <span data-ttu-id="b4f1f-120">Opprett en beregning som har følgende uttrykk:</span><span class="sxs-lookup"><span data-stu-id="b4f1f-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="b4f1f-121">*Resultat* = *inndata* × *prosent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="b4f1f-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="b4f1f-122">I dette tilfellet blir ikke heltallsresultatet alltid avrundet riktig.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="b4f1f-123">Inndataene er for eksempel 1 000, og prosenten er 2,40.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="b4f1f-124">Derfor forventer du at heltallsresultatet er 24, fordi 2,40 prosent av 1 000 er 24 (eller 24,00 i desimalformat).</span><span class="sxs-lookup"><span data-stu-id="b4f1f-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="b4f1f-125">Resultatet vises i stedet som 23.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="b4f1f-126">Når prosenten er 2,39, avrundes imidlertid beregningen til 24 i stedet for 23.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="b4f1f-127">Når prosenten er 2,50, avrundes beregningen til 25 som forventet.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b4f1f-128">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b4f1f-128">Issue resolution</span></span>

<span data-ttu-id="b4f1f-129">Dette problemet oppstår på grunn av måten som Microsoft Solver Foundation internt representerer tall ved hjelp av brøker.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="b4f1f-130">I det foregående eksemplet representeres resultatet av beregningen der prosenten er 2,40 som 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="b4f1f-131">Når .NET sender denne verdien som et heltall, returnerer den 23.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="b4f1f-132">Denne virkemåten vil ikke bli endret fordi andre scenarioer er avhengige av den.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="b4f1f-133">I det foregående eksemplet kan du løse problemet ved å introdusere et ekstra desimalattributt og en beregning.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="b4f1f-134">Du kan for eksempel definere følgende attributter i en produksjonskonfigurasjonsmodell:</span><span class="sxs-lookup"><span data-stu-id="b4f1f-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="b4f1f-135">Inndata (heltall)</span><span class="sxs-lookup"><span data-stu-id="b4f1f-135">Input (integer)</span></span>
- <span data-ttu-id="b4f1f-136">Prosent (desimal)</span><span class="sxs-lookup"><span data-stu-id="b4f1f-136">Percent (decimal)</span></span>
- <span data-ttu-id="b4f1f-137">ResultDecimal (desimal)</span><span class="sxs-lookup"><span data-stu-id="b4f1f-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="b4f1f-138">ResultInteger (heltall)</span><span class="sxs-lookup"><span data-stu-id="b4f1f-138">ResultInteger (integer)</span></span>

<span data-ttu-id="b4f1f-139">Du kan deretter legge til følgende beregninger:</span><span class="sxs-lookup"><span data-stu-id="b4f1f-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="b4f1f-140">*ResultDecimal* = *inndata* × *prosent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="b4f1f-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="b4f1f-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="b4f1f-141">*ResultInteger* = *ResultDecimal*</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]