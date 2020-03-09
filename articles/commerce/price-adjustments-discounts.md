---
title: Prisjusteringer og rabatter
description: Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dfaacfa7681258e3b2273083017c0c398d566651
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023595"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="44e09-103">Prisjusteringer og rabatter</span><span class="sxs-lookup"><span data-stu-id="44e09-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="44e09-104">Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="44e09-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="44e09-105">I Commerce kan du justere prisene for produkter, og du kan også definere rabatter som gjelder for en linjevare eller en transaksjon på salgsstedet, i en salgsordre via et telefonsenter eller i en elektronisk ordre.</span><span class="sxs-lookup"><span data-stu-id="44e09-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="44e09-106">Både prisjusteringer og rabatter kan knyttes til prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="44e09-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="44e09-107">Du kan angi én enkelt startdato og sluttdato eller en regelmessig periode, en rabattkode og noen ytterligere attributter for både prisjusteringer og rabatter.</span><span class="sxs-lookup"><span data-stu-id="44e09-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="44e09-108">Prisjusteringer og rabatter kan brukes på produkter, varianter eller hierarkier.</span><span class="sxs-lookup"><span data-stu-id="44e09-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="44e09-109">Hvis mer enn én rabatt gjelder for et produkt, kan en kunde få enten en av rabattene eller en kombinert rabatt, avhengig av konfigurasjonen av rabatten.</span><span class="sxs-lookup"><span data-stu-id="44e09-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="44e09-110">Commerce bruker automatisk rabatten eller kombinasjon av rabatter som gir den beste prisen til kunden.</span><span class="sxs-lookup"><span data-stu-id="44e09-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="44e09-111">Når du definerer en prisjustering eller rabatt, må du bekrefte at prisgrupper tilordnes til riktige kanaler, kataloger, tilknytninger eller fordelsprogrammer som du vil at rabatten skal gjelde for.</span><span class="sxs-lookup"><span data-stu-id="44e09-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="44e09-112">Hvis du i tillegg vil generere rabatt-ID-en automatisk, kan du definere nummerserier på **Handelsparametere**-siden før du definerer en ny rabatt eller prisjustering.</span><span class="sxs-lookup"><span data-stu-id="44e09-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="44e09-113">Du kan slette en prisjustering eller rabatt.</span><span class="sxs-lookup"><span data-stu-id="44e09-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="44e09-114">Statistisk informasjon går imidlertid tapt.</span><span class="sxs-lookup"><span data-stu-id="44e09-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="44e09-115">Rabattyper</span><span class="sxs-lookup"><span data-stu-id="44e09-115">Types of discounts</span></span>

<span data-ttu-id="44e09-116">Det finnes fire typer rabatter:</span><span class="sxs-lookup"><span data-stu-id="44e09-116">There are four types of discounts:</span></span>

- <span data-ttu-id="44e09-117">**Enkel rabatt** – en enkelt prosent eller et enkelt beløp.</span><span class="sxs-lookup"><span data-stu-id="44e09-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="44e09-118">**Kvantumsrabatt** – en rabatt som brukes når to eller flere varer som kjøpes.</span><span class="sxs-lookup"><span data-stu-id="44e09-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="44e09-119">**Samlerabatt** – en rabatt som brukes ved kjøp av en bestemt kombinasjon av produkter.</span><span class="sxs-lookup"><span data-stu-id="44e09-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="44e09-120">**Terskelrabatt** – en rabatt som brukes når totalen for transaksjonen er mer enn et bestemt beløp.</span><span class="sxs-lookup"><span data-stu-id="44e09-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="44e09-121">Både prisjusteringer og rabatter kan knyttes til prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="44e09-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="44e09-122">Prisgrupper kan deretter knyttes til kanaler, kataloger, tilknytninger og fordelsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="44e09-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>