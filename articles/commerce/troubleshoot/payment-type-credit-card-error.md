---
title: Betalingstypen må være kredittkortfeil på salgsordresiden
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe deg når det vises en feilmelding på salgsordresiden etter at en ordre er synkronisert.
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
ms.openlocfilehash: eabc64acc74645c7e6c7c4ab5794ed9fdb9dc997
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801681"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="28c98-103">Feilen Betalingstypen må være kredittkort på salgsordresiden</span><span class="sxs-lookup"><span data-stu-id="28c98-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28c98-104">Dette emnet inneholder feilsøkingsveiledning som kan hjelpe deg når det vises en feilmelding på salgsordresiden etter at en ordre er synkronisert.</span><span class="sxs-lookup"><span data-stu-id="28c98-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="28c98-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="28c98-105">Description</span></span>

<span data-ttu-id="28c98-106">Når du åpner salgsordresiden etter at du har synkronisert en ordre, får du følgende feilmelding: Betalingstypen må være kredittkort ettersom kredittkortnummeret er angitt.</span><span class="sxs-lookup"><span data-stu-id="28c98-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Betalingstype må være kredittkortfeil](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="28c98-108">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="28c98-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="28c98-109">Angi betalingstypen i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="28c98-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="28c98-110">Gå til **Kunder \> Betalingsoppsett \> Betalingsbetingelser**.</span><span class="sxs-lookup"><span data-stu-id="28c98-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="28c98-111">Velg betalingsbetingelsene til venstre.</span><span class="sxs-lookup"><span data-stu-id="28c98-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="28c98-112">Kontroller at det er merket av for **Kredittkort** i feltet **Betalingstype**.</span><span class="sxs-lookup"><span data-stu-id="28c98-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28c98-113">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="28c98-113">Additional resources</span></span>

[<span data-ttu-id="28c98-114">Postering av elektroniske salg og betalinger</span><span class="sxs-lookup"><span data-stu-id="28c98-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
