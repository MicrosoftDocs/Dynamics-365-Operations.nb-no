---
title: Betalinger utlignes automatisk før ordrer faktureres eller sendes
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en betaling utlignes i Adyen-portalen rett etter at en ordre er lagt inn, selv om salgsordren ikke er fakturert eller sendt.
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
ms.openlocfilehash: 43fe90cf99ddbe42dc89685e7fc747ded5a285c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801657"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="f9c4a-103">Betalinger utlignes automatisk før ordrer faktureres eller sendes</span><span class="sxs-lookup"><span data-stu-id="f9c4a-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9c4a-104">Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en betaling utlignes i Adyen-portalen rett etter at en ordre er lagt inn, selv om salgsordren ikke er fakturert eller sendt.</span><span class="sxs-lookup"><span data-stu-id="f9c4a-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="f9c4a-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f9c4a-105">Description</span></span>

<span data-ttu-id="f9c4a-106">Etter at en ordre er plassert, blir betalingen umiddelbart utlignet i Adyen-portalen, selv om salgsordren ikke er fakturert eller sendt.</span><span class="sxs-lookup"><span data-stu-id="f9c4a-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="f9c4a-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="f9c4a-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="f9c4a-108">Konfigurere manuell henting for e-handelbetalinger i Adyen-portalen</span><span class="sxs-lookup"><span data-stu-id="f9c4a-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="f9c4a-109">Hvis du vil konfigurere manuell henting for e-handelsbetalinger i Adyen-portalen, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="f9c4a-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="f9c4a-110">Logg på Adyen-portalen.</span><span class="sxs-lookup"><span data-stu-id="f9c4a-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="f9c4a-111">Velg forretningskontoen for e-handelskanalen øverst til høyre.</span><span class="sxs-lookup"><span data-stu-id="f9c4a-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="f9c4a-112">Velg **Konto** i det øverste navigasjonsfeltet, og velg deretter **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f9c4a-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="f9c4a-113">Velg **manuell** i feltet **Opptaksforsinkelse**.</span><span class="sxs-lookup"><span data-stu-id="f9c4a-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Innstillingen Opptaksforsinkelse i Adyen-portalen](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="f9c4a-115">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f9c4a-115">Additional resources</span></span>

[<span data-ttu-id="f9c4a-116">Lagring av Adyen-betaling</span><span class="sxs-lookup"><span data-stu-id="f9c4a-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="f9c4a-117">Dynamics 365 Payment Connector for Adyen</span><span class="sxs-lookup"><span data-stu-id="f9c4a-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="f9c4a-118">Konfigurere Adyen-betalingskobling for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f9c4a-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
