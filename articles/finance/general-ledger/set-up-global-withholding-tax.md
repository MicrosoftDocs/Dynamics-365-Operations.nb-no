---
title: Definere global kildeskatt
description: Dette emnet viser en liste over trinnene for å definere global kildeskatt for salg og kjøp.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7ee577651694f0553447d6e9d0851402a586f363
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060775"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="f6444-103">Definere global kildeskatt</span><span class="sxs-lookup"><span data-stu-id="f6444-103">Set up global withholding tax</span></span>

<span data-ttu-id="f6444-104">Dette emnet viser en liste over trinnene for å definere global kildeskatt for salg og kjøp.</span><span class="sxs-lookup"><span data-stu-id="f6444-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="f6444-105">Definer kildeskattmyndighetene på siden for **Myndigheter for kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="f6444-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="f6444-106">Definer utligningsperioder for kildeskatt på siden **Utligningsperioder for kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="f6444-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="f6444-107">Definer posteringsgruppe for kildeskatt på siden **Kildeskatt > finansposteringsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="f6444-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="f6444-108">**Kildeskatt**-kontoen blir tilordnet med en hovedkonto med **Posteringstypen** Kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="f6444-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="f6444-109">**Kildeskattmotkonto**-kontoen blir også tilordnet med en hovedkonto med **Posteringstypen** "Kildeskattmotkonto".</span><span class="sxs-lookup"><span data-stu-id="f6444-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="f6444-110">Gå til **Økonomimodul > Kontoplan > Kontoer > Hovedkontoer**, og konfigurer **Posteringstype** i underskjemaet for **Posteringsvalidering** for hovedkontoene.</span><span class="sxs-lookup"><span data-stu-id="f6444-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="f6444-111">Definer kildeskattkoder på siden for **Kildeskattkoder**.</span><span class="sxs-lookup"><span data-stu-id="f6444-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="f6444-112">Definer kildeskattgrupper på siden for **Kildeskattgrupper**.</span><span class="sxs-lookup"><span data-stu-id="f6444-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="f6444-113">Definer inntektstyper for kildeskatt på siden **Kildeskattinntekt** **typer**.</span><span class="sxs-lookup"><span data-stu-id="f6444-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="f6444-114">Definer kildeskattgrupper på siden for **Kildeskattegrupper for vare** for en vare eller tjeneste.</span><span class="sxs-lookup"><span data-stu-id="f6444-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="f6444-115">Definer **Minste fakturabeløp** på siden **Parametere for økonomimodul > Kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="f6444-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>
