---
title: Prisjusteringer og rabatter
description: Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i Dynamics 365 Commerce.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240948"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="b41ef-103">Prisjusteringer og rabatter</span><span class="sxs-lookup"><span data-stu-id="b41ef-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b41ef-104">Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b41ef-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b41ef-105">I Commerce kan du justere prisene for produkter, og du kan også definere rabatter som gjelder for en linjevare eller en transaksjon på salgsstedet, i en salgsordre via et telefonsenter eller i en elektronisk ordre.</span><span class="sxs-lookup"><span data-stu-id="b41ef-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="b41ef-106">Både prisjusteringer og rabatter kan knyttes til prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="b41ef-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="b41ef-107">Du kan angi én enkelt startdato og sluttdato eller en regelmessig periode, en rabattkode og noen ytterligere attributter for både prisjusteringer og rabatter.</span><span class="sxs-lookup"><span data-stu-id="b41ef-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="b41ef-108">Prisjusteringer og rabatter kan brukes på produkter, varianter eller hierarkier.</span><span class="sxs-lookup"><span data-stu-id="b41ef-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="b41ef-109">Hvis mer enn én rabatt gjelder for et produkt, kan en kunde få enten en av rabattene eller en kombinert rabatt, avhengig av konfigurasjonen av rabatten.</span><span class="sxs-lookup"><span data-stu-id="b41ef-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="b41ef-110">Commerce bruker automatisk rabatten eller kombinasjon av rabatter som gir den beste prisen til kunden.</span><span class="sxs-lookup"><span data-stu-id="b41ef-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="b41ef-111">Når du definerer en prisjustering eller rabatt, må du bekrefte at prisgrupper tilordnes til riktige kanaler, kataloger, tilknytninger eller fordelsprogrammer som du vil at rabatten skal gjelde for.</span><span class="sxs-lookup"><span data-stu-id="b41ef-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="b41ef-112">Hvis du i tillegg vil generere rabatt-ID-en automatisk, kan du definere nummerserier på **Handelsparametere**-siden før du definerer en ny rabatt eller prisjustering.</span><span class="sxs-lookup"><span data-stu-id="b41ef-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="b41ef-113">Du kan slette en prisjustering eller rabatt.</span><span class="sxs-lookup"><span data-stu-id="b41ef-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="b41ef-114">Statistisk informasjon går imidlertid tapt.</span><span class="sxs-lookup"><span data-stu-id="b41ef-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="b41ef-115">Rabattyper</span><span class="sxs-lookup"><span data-stu-id="b41ef-115">Types of discounts</span></span>

<span data-ttu-id="b41ef-116">Det finnes mange typer rabatter:</span><span class="sxs-lookup"><span data-stu-id="b41ef-116">There are many types of discounts:</span></span>

- <span data-ttu-id="b41ef-117">**Enkel rabatt** – en enkelt prosent eller et enkelt beløp.</span><span class="sxs-lookup"><span data-stu-id="b41ef-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="b41ef-118">**Kvantumsrabatt** – en rabatt som brukes når to eller flere varer som kjøpes.</span><span class="sxs-lookup"><span data-stu-id="b41ef-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="b41ef-119">**Samlerabatt** – en rabatt som brukes ved kjøp av en bestemt kombinasjon av produkter.</span><span class="sxs-lookup"><span data-stu-id="b41ef-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="b41ef-120">**Terskelrabatt** – en rabatt som brukes når totalen for transaksjonen er mer enn et bestemt beløp.</span><span class="sxs-lookup"><span data-stu-id="b41ef-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="b41ef-121">**Betalingsmiddelbasert rabatt** – En rabatt som brukes når totalen for transaksjonen er mer enn et bestemt beløp, og en bestemt betalingstype (for eksempel kontant, kredit- eller debetkort) brukes til betaling.</span><span class="sxs-lookup"><span data-stu-id="b41ef-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="b41ef-122">**Leveringsrabatt** – En rabatt som brukes når totalen for transaksjonen er mer enn et bestemt beløp og en bestemt leveringsmåte (for eksempel forsendelse på to dager eller over natten) brukes på ordren.</span><span class="sxs-lookup"><span data-stu-id="b41ef-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="b41ef-123">Både prisjusteringer og rabatter kan knyttes til prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="b41ef-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="b41ef-124">Prisgrupper kan deretter knyttes til kanaler, kataloger, tilknytninger og fordelsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="b41ef-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="b41ef-125">Samlerabatten og terskelrabatten har henholdsvis egenskapene «Regn med ikke-rabatterte produkter» og «Tell ikke-rabatterte produkter mot terskel».</span><span class="sxs-lookup"><span data-stu-id="b41ef-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="b41ef-126">Hvis disse egenskapene er aktivert, kan en vare som ikke kvalifiserer for rabatt, likevel bidra til å kvalifisere en transaksjon for rabatten, men den ikke-kvalifiserte varen blir ikke rabattert.</span><span class="sxs-lookup"><span data-stu-id="b41ef-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="b41ef-127">Hvis du for eksempel oppretter en samlerabatt med to linjer, A og B, der en kunde skal få 10 % rabatt på begge varene, men der det er merket av for Hindre alle rabatter for vare A, gjør dette vanligvis at vare A ikke blir tatt med i rabatten.</span><span class="sxs-lookup"><span data-stu-id="b41ef-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="b41ef-128">Hvis egenskapen «Regn med ikke-rabatterte produkter» er aktivert, kan imidlertid vare A brukes til å kvalifisere for samlerabatten, men rabatten på 10 % brukes bare på vare B. En tilsvarende logikk gjelder for terskelrabatten.</span><span class="sxs-lookup"><span data-stu-id="b41ef-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="b41ef-129">Egenskapen «Tell ikke-rabatterte produkter mot terskel» har imidlertid en tilleggsfunksjon sammenlignet med egenskapen «Regn med ikke-rabatterte produkter» for samlerabatten.</span><span class="sxs-lookup"><span data-stu-id="b41ef-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="b41ef-130">Hvis terskelrabatten er aktivert og det finnes en vare som har en eksisterende rabatt som gjør at andre rabatter ikke kan gjelde for varen, kvalifiserer prisen som betales for denne varen, mot terskelen, men tilleggsrabatten blir ikke gjeldende for denne varen.</span><span class="sxs-lookup"><span data-stu-id="b41ef-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
