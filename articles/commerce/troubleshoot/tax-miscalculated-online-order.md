---
title: Avgifter på elektroniske ordrer beregnes feil
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe når avgifter på nettordrer beregnes feil, eller når mva-gruppen på salgslinje ikke er riktig angitt.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7f71add679e1d24f80db8ce3990058b591128ec1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801417"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="4f484-103">Avgifter på elektroniske ordrer beregnes feil</span><span class="sxs-lookup"><span data-stu-id="4f484-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f484-104">Dette emnet gir feilsøkingsveiledning som kan hjelpe når avgifter på nettordrer beregnes feil, eller når mva-gruppen på salgslinje ikke er riktig angitt.</span><span class="sxs-lookup"><span data-stu-id="4f484-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="4f484-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4f484-105">Description</span></span>

<span data-ttu-id="4f484-106">Når en e-handelsordre blir lagt inn, blir avgiftene feil beregnet, eller mva-gruppen på salgslinjen er feil angitt.</span><span class="sxs-lookup"><span data-stu-id="4f484-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="4f484-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="4f484-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="4f484-108">Konfigurere merverdiavgift for en detaljhandelsbutikk i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="4f484-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="4f484-109">Hvis du vil konfigurere merverdiavgift for en detaljhandelsbutikk i Commerce Headquarters, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="4f484-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4f484-110">Gå til **Detaljhandel og handel \> Kanaler \> Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="4f484-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="4f484-111">Velg butikken du skal konfigurere merverdiavgift for.</span><span class="sxs-lookup"><span data-stu-id="4f484-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="4f484-112">I hurtigfanen **Generelt** konfigurerer du mva-inforamsjonen for butikken i delen **Merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="4f484-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="4f484-113">For produkthenting fra en butikk kommer mva-gruppen fra butikken som er valgt for henting.</span><span class="sxs-lookup"><span data-stu-id="4f484-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="4f484-114">Du finner mer informasjon under [Angi andre mva-alternativer for butikker](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="4f484-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="4f484-115">Konfigurere merverdiavgift for en kundes adresse i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="4f484-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="4f484-116">Hvis du vil konfigurere merverdiavgift for en kundes adresse i Commerce Headquarters, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="4f484-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4f484-117">Gå til **Kunder \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="4f484-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="4f484-118">Velg kunden du skal konfigurere merverdiavgift for.</span><span class="sxs-lookup"><span data-stu-id="4f484-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="4f484-119">I hurtigfanen **Adresser** velger du adressen du vil konfigurere merverdiavgift for, velger **Flere alternativer**, og velger deretter **Avansert**.</span><span class="sxs-lookup"><span data-stu-id="4f484-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="4f484-120">I hurtigfanen **Generelt** velger du **Mva-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="4f484-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="4f484-121">I feltet **Merverdiavgift** velger du den riktige verdien.</span><span class="sxs-lookup"><span data-stu-id="4f484-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="4f484-122">For forsendelse som omfatter merverdiavgift på kundens adresse, bestemmer leveringsadressen for linjen mva-gruppen for linjen.</span><span class="sxs-lookup"><span data-stu-id="4f484-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="4f484-123">Hvis kunden sender til en eksisterende adresse som har en mva-gruppe som allerede er konfigurert, vil den eksisterende avgiftsgruppen bli brukt.</span><span class="sxs-lookup"><span data-stu-id="4f484-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="4f484-124">Som standard har ikke adresser noen mva-gruppe når de opprettes.</span><span class="sxs-lookup"><span data-stu-id="4f484-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="4f484-125">Konfigurere generelle mva-grupper i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="4f484-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="4f484-126">Hvis du vil konfigurere generelle mva-grupper i Commerce Headquarters, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="4f484-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4f484-127">Gå til **Avgift \> Indirekte avgifter \> Merverdiavgift \> Mva-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="4f484-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="4f484-128">Velg mva-gruppen du vil konfigurere, til venstre.</span><span class="sxs-lookup"><span data-stu-id="4f484-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="4f484-129">Konfigurer avgiftene for mva-gruppen i hurtigfanen **Destinasjonsbasert avgift for detaljhandel**.</span><span class="sxs-lookup"><span data-stu-id="4f484-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="4f484-130">For forsendelse som ikke innbærer merverdiavgift på kundens adresse, bestemmer leveringsadressen for linjen og de destinasjonsbaserte avgiftene som er konfigurert for mva-gruppen, mva-gruppen.</span><span class="sxs-lookup"><span data-stu-id="4f484-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="4f484-131">Hvis du vil ha mer informasjon, kan du se [Definere avgifter for nettbutikker basert på destinasjon](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="4f484-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f484-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4f484-132">Additional resources</span></span>

[<span data-ttu-id="4f484-133">Konfigurere merverdiavgift for elektroniske ordrer</span><span class="sxs-lookup"><span data-stu-id="4f484-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
