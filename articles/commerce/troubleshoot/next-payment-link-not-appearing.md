---
title: Lagring for mitt neste betalingsalternativ vises ikke
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe når avmerkingsboksen Lagre for neste betaling ikke vises under Betalingsmåte på betalingssiden til et e-handelsområde.
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
ms.openlocfilehash: 7e3156d1aa9a05dc5d159b6f9b33ae341de640bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801705"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="d36c3-103">Alternativet Lagre for min neste betaling vises ikke</span><span class="sxs-lookup"><span data-stu-id="d36c3-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d36c3-104">Dette emnet gir feilsøkingsveiledning som kan hjelpe når avmerkingsboksen **Lagre for neste betaling** ikke vises under **Betalingsmåte** på betalingssiden til et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="d36c3-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="d36c3-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d36c3-105">Description</span></span>

<span data-ttu-id="d36c3-106">Avmerkingsboksen **Lagre for min neste betaling** vises ikke i delen **Betalingsmåte** på betalingssiden til en e-handel.</span><span class="sxs-lookup"><span data-stu-id="d36c3-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="d36c3-107">Illustrasjonen nedenfor viser et eksempel på en utsjekkingsside som inneholder avmerkingsboksen **Lagre for min neste betaling**.</span><span class="sxs-lookup"><span data-stu-id="d36c3-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Lagre for min neste betaling i betalingsmodulen](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="d36c3-109">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="d36c3-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="d36c3-110">Kontroller at Dynamics 365 Payment Connector for Adyen er riktig konfigurert i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="d36c3-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="d36c3-111">Hvis du vil kontrollere at Dynamics 365 Payment Connector for Adyen er riktig konfigurert i Commerce Headquarters, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="d36c3-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d36c3-112">Gå til **Detaljhandel og handel \> Kanaler \> Nettbutikker**.</span><span class="sxs-lookup"><span data-stu-id="d36c3-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="d36c3-113">Velg nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="d36c3-113">Select the online store.</span></span>
1. <span data-ttu-id="d36c3-114">I hurtigfanen **Betalingskontoer** kontrollerer du at feltet **Tillat lagring av betalingsinformasjon i e-handel** er satt til **Sann**.</span><span class="sxs-lookup"><span data-stu-id="d36c3-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Tillat lagring av betalingsinformasjon i e-handelsfelt i Commerce Headquarters](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="d36c3-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d36c3-116">Additional resources</span></span>

[<span data-ttu-id="d36c3-117">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="d36c3-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="d36c3-118">Lagre betalingsmåter på nett med Adyen-koblingen</span><span class="sxs-lookup"><span data-stu-id="d36c3-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
