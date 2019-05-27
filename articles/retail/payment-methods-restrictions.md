---
title: Begrense betalingsmåter for returer uten en kvittering
description: Dette emnet beskriver hvordan bestemte betalingstyper kan være begrenset for refusjon hvis returer gjøres uten et mottak.
author: rapraj
manager: AnnBe
ms.date: 013/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 6e2c32aae06ce7bbdde30809d7a197f43b856af1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564358"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="82669-103">Begrense betalingsmåter for returer uten en kvittering</span><span class="sxs-lookup"><span data-stu-id="82669-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="82669-104">Hver betalingstype en forhandler godtar, må konfigureres når systemet defineres.</span><span class="sxs-lookup"><span data-stu-id="82669-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="82669-105">Dette emnet beskriver hvordan bestemte betalingstyper kan være begrenset for refusjon hvis returer gjøres uten et mottak.</span><span class="sxs-lookup"><span data-stu-id="82669-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="82669-106">Definere betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="82669-106">Set up payment methods</span></span>

<span data-ttu-id="82669-107">Du må fullføre følgende oppgaver hvis du vil definere betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="82669-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="82669-108">Opprett betalingsmåtene som godtas av hele organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="82669-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="82669-109">Opprett korttyper og kortnumre for hele organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="82669-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="82669-110">Hvis kredittkortene eller debetkortene godtas, må du opprette én betalingsmetode for kort og deretter opprette korttypene og kortnumrene for hele organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="82669-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="82669-111">Definere betalingsmåter i butikker.</span><span class="sxs-lookup"><span data-stu-id="82669-111">Set up store payment methods.</span></span> <span data-ttu-id="82669-112">Knytt betalingsmåter til hver butikk, og angi deretter de butikkspesifikke innstillingene for hvert betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="82669-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="82669-113">Definer kortbetalingsmåter for butikker.</span><span class="sxs-lookup"><span data-stu-id="82669-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="82669-114">Fullfør kortoppsettet for alle kortbetalingsmåter som butikken godtar.</span><span class="sxs-lookup"><span data-stu-id="82669-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="82669-115">![Oppsett av detaljhandelsbutikk](media/NoReceiptReturns1.png "Oppsett av detaljhandelsbutikk")</span><span class="sxs-lookup"><span data-stu-id="82669-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="82669-116">Begrense betalingsmåter for returer uten en kvittering</span><span class="sxs-lookup"><span data-stu-id="82669-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="82669-117">For hver betalingsmåte for butikk, på siden **Administrasjon av detaljhandelsbutikk** under **Returer uten kvittering**, sett **Begrens for refusjoner uten kvittering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="82669-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="82669-118">Standardverdien for av/på er **Nei**, som sikrer at betalingsmåten er tillatt for refusjoner.</span><span class="sxs-lookup"><span data-stu-id="82669-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="82669-119">Når **Begrens for refusjoner uten kvittering** er satt til **Ja**, tillates ikke den valgte betalingsmåten for refusjoner.</span><span class="sxs-lookup"><span data-stu-id="82669-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="82669-120">![Betalingsmåte for detaljhandelsbutikk](media/NoReceiptReturns3.png "Betalingsmåte for detaljhandelsbutikk")</span><span class="sxs-lookup"><span data-stu-id="82669-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="82669-121">Når en kasserer legger til en betalingsmåte som er begrenset for refusjon uten kvittering, vises en melding for å bekrefte de akseptable betalingsmåtene.</span><span class="sxs-lookup"><span data-stu-id="82669-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="82669-122">![Godkjente betalingsmåter](media/NoReceiptReturns4.png "Godkjente betalingsmåter")</span><span class="sxs-lookup"><span data-stu-id="82669-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="82669-123">Hvis en transaksjon har både en retur med kvittering og en retur uten kvittering, fremtvinges ikke begrensningsbetingelsene, fordi transaksjonen vil være en returarbeidsflyt med kvittering.</span><span class="sxs-lookup"><span data-stu-id="82669-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

