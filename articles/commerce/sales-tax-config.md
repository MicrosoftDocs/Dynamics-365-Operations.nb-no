---
title: Konfigurer merverdiavgift for nettordrer
description: Dette emnet gir en oversikt over valg av mva-grupper for ulike nettordretyper i Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 56621bb9658b71551c7312aa47812903914bc888
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031795"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="3fe4a-103">Konfigurer merverdiavgift for nettordrer</span><span class="sxs-lookup"><span data-stu-id="3fe4a-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3fe4a-104">Dette emnet gir en oversikt over valg av avgiftsgrupper for ulike nettordretyper.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="3fe4a-105">Det kan hende at e-handelskanalen vil støtte alternativer som levering eller henting for nettordrer.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="3fe4a-106">Mva-relevansen er basert på alternativet som er valgt av nettbrukerne.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="3fe4a-107">Når en områdekunde velger å kjøpe en vare på nettet og mottar den levert til en adresse, blir merverdiavgiften bestemt på grunnlag av kundens mva-gruppe for leveringsadresse.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="3fe4a-108">Når en kunde velger å hente en kjøpt vare i en butikk, bestemmes merverdiavgiften basert på innstillingen for mva-gruppen for butikken den hentes i.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="3fe4a-109">Bestillinger sendt til en kundeadresse</span><span class="sxs-lookup"><span data-stu-id="3fe4a-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="3fe4a-110">Vanligvis defineres avgifter for nettbestillinger som sender til kundeadresser, av destinasjonen.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="3fe4a-111">Hver mva-gruppe har en destinasjonsbasert mva-konfigurasjon der virksomheten kan definere måldetaljer som land/område, fylke, region og poststed i et hierarkisk skjema.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="3fe4a-112">Når en nettordre bestilles, bruker Commerce-avgiftsmotoren leveringsadressen for hver linjevare i ordren, og finner mva-grupper med samsvarende målbaserte avgiftskriterier.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="3fe4a-113">For en nettordre med en leveringsadresse for linjevare til San Francisco, California, vil avgiftsmotoren for eksempel finne mva-gruppen og mva-koden for California, og deretter beregne merverdiavgift for hver linjevare i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="3fe4a-114">Kundebaserte avgiftsgrupper</span><span class="sxs-lookup"><span data-stu-id="3fe4a-114">Customer-based tax groups</span></span>

<span data-ttu-id="3fe4a-115">I Commerce Headquarters finnes det to steder der kundeavgiftsgrupper er konfigurert:</span><span class="sxs-lookup"><span data-stu-id="3fe4a-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="3fe4a-116">**Kundens profil**</span><span class="sxs-lookup"><span data-stu-id="3fe4a-116">**Customer's profile**</span></span>
- <span data-ttu-id="3fe4a-117">**Kundens leveringsadresse**</span><span class="sxs-lookup"><span data-stu-id="3fe4a-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="3fe4a-118">Hvis en kundes profil har en avgiftsgruppe konfigurert</span><span class="sxs-lookup"><span data-stu-id="3fe4a-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="3fe4a-119">En kundes profilpost i hovedkontoret kan ha en avgiftsgruppe konfigurert, men for nettordrer vil ikke avgiftsgruppen som er konfigurert i en kundes profil, bli brukt av avgiftsmotoren.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="3fe4a-120">Hvis en kundes leveringsadresse har en avgiftsgruppe konfigurert</span><span class="sxs-lookup"><span data-stu-id="3fe4a-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="3fe4a-121">Hvis kundens leveringsadressepost har en avgiftsgruppe konfigurert, og en nettordre (eller linjevare) skal sendes til kundens leveringsadresse, vil avgiftsgruppen som er konfigurert i kundens adressepost, bli brukt av avgiftsmotoren til avgiftsberegning.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="3fe4a-122">Konfigurer en avgiftsgruppe for en kundes leveringsadressepost</span><span class="sxs-lookup"><span data-stu-id="3fe4a-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="3fe4a-123">Følg denne fremgangsmåten for å konfigurere en avgiftsgruppe for kundens leveringsadressepost i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="3fe4a-124">Gå til **Alle kunder**, og velg deretter ønsket kunde.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="3fe4a-125">Velg ønsket adresse i hurtigfanen **Adresser**, og velg deretter **Flere alternativer \> Avansert**.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="3fe4a-126">Angi merverdiavgiftsverdien etter behov under fanen **Generelt** på **Administrer adresser**-siden.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="3fe4a-127">Avgiftsgruppen defineres ved hjelp av leveringsadressen for ordrelinjen, og de destinasjonsbaserte avgiftene konfigureres ved selve avgiftsgruppen.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="3fe4a-128">Hvis du vil ha mer informasjon, kan du se [Definere avgifter for nettbutikker basert på destinasjon](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="3fe4a-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="3fe4a-129">Hent ordre i butikk</span><span class="sxs-lookup"><span data-stu-id="3fe4a-129">Order pickup in store</span></span>

<span data-ttu-id="3fe4a-130">For ordrelinjer der henting i butikk eller henting utenfor butikk angitt, vil avgiftsgruppen fra det valgte butikken for henting, bli brukt.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="3fe4a-131">Hvis du vil ha mer informasjon om hvordan du konfigurerer avgiftsgruppen for en gitt butikk, kan du se [Angi andre mva-alternativer for butikker](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="3fe4a-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="3fe4a-132">Når en ordrelinje hentes i en butikk, vil kundens adresseavgiftsinnstillinger (hvis konfigurert) bli ignorert av avgiftsmotoren, og avgiftskonfigurasjonen til butikken det hentes i, blir brukt.</span><span class="sxs-lookup"><span data-stu-id="3fe4a-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="3fe4a-133">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3fe4a-133">Additional resources</span></span>

[<span data-ttu-id="3fe4a-134">Oversikt over merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="3fe4a-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="3fe4a-135">Beregningsmåter for merverdiavgift i grunnlagsfeltet</span><span class="sxs-lookup"><span data-stu-id="3fe4a-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="3fe4a-136"> Mva-tilordning og overstyringer</span><span class="sxs-lookup"><span data-stu-id="3fe4a-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="3fe4a-137">Hele beløp og alternativer for intervallberegning for mva-koder</span><span class="sxs-lookup"><span data-stu-id="3fe4a-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="3fe4a-138">Beregning av mva-fritak</span><span class="sxs-lookup"><span data-stu-id="3fe4a-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 

