---
title: Alternativer for å hindre rabatter for detaljhandelsprodukter
description: Det finnes ulike årsaker til hvorfor forhandlere vil forhindre at noen produkter rabatteres, fra en kampanje eller ved salget på salgsstedet.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f5037067917290f21f681d2446a0e1ab0e31228c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231206"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="669f9-103">Alternativer for å hindre rabatter for detaljhandelsprodukter</span><span class="sxs-lookup"><span data-stu-id="669f9-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="669f9-104">Det finnes ulike årsaker til hvorfor forhandlere vil forhindre at noen produkter rabatteres, fra en kampanje eller ved salget på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="669f9-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="669f9-105">De følgende alternativene, som finnes på **Handel**-kategorien for frigitte produkter, gjør at produktet kan konfigureres for å hindre alle eller manuelle rabatter.</span><span class="sxs-lookup"><span data-stu-id="669f9-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="669f9-106">Innstillingene kan også angis på kategorinivå fra kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="669f9-106">The settings can also be specified at the category level from the category hierarchy.</span></span>

- <span data-ttu-id="669f9-107">**Forhindre alle rabatter** – Velg dette alternativet for å forhindre at alle typer rabatter brukes på dette produktet.</span><span class="sxs-lookup"><span data-stu-id="669f9-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="669f9-108">Dette inkluderer kampanjer som samlerabatt, antalls- og terskelrabatter, i tillegg til rabatter for manuelle linjerabatter og transaksjonsrabatter som brukes under et salg av en POS-bruker.</span><span class="sxs-lookup"><span data-stu-id="669f9-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="669f9-109">**Hindre manuelle rabatter** – Velg dette alternativet for bare å hindre de manuelle linjerabattene eller transaksjonsrabattene som brukes under et salg av en POS-bruker.</span><span class="sxs-lookup"><span data-stu-id="669f9-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="669f9-110">Produkter med dette alternativet valgt er fremdeles kvalifisert for kampanjer, for eksempel samlerabatt, antalls- og terskelrabatter.</span><span class="sxs-lookup"><span data-stu-id="669f9-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="669f9-111">Disse innstillingene begrenser ikke operasjonen for prisoverstyring, fordi det angir basisprisen og behandles ikke som en rabatt.</span><span class="sxs-lookup"><span data-stu-id="669f9-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="669f9-112">[![Hindre rabatter-felt](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="669f9-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]