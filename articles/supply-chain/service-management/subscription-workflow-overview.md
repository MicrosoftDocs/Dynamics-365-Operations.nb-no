---
title: Oversikt over abonnementsarbeidsflyt
description: Dette emnet gir en oversikt over abonnementsarbeidsflyt.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05111ab53e8bf19bb25869155284cdc9d6ea3b2a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242283"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="86f8e-103">Oversikt over abonnementsarbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="86f8e-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="86f8e-104">Du er abonnementsadministrator for et lysselskap som tilbyr abonnement for vedlikehold av lysrigger.</span><span class="sxs-lookup"><span data-stu-id="86f8e-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="86f8e-105">En kunde tar kontakt for å kjøpe et årlig sabonnement på vedlikehold av lysrigger.</span><span class="sxs-lookup"><span data-stu-id="86f8e-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="86f8e-106">Definere abonnement</span><span class="sxs-lookup"><span data-stu-id="86f8e-106">Setting up subscriptions</span></span>

<span data-ttu-id="86f8e-107">Når du skal definere et abonnement, må du først opprette en abonnementsgruppe for den nye tjenesteavtalen, eller bekrefte at det finnes en abonnementsgruppe.</span><span class="sxs-lookup"><span data-stu-id="86f8e-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="86f8e-108">Hvis det finnes en abonnementsgruppe, må du angi den til å fakturere kunden årlig og utligne salgsinntekter hver måned i året.</span><span class="sxs-lookup"><span data-stu-id="86f8e-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="86f8e-109">Hvis du vil ha mer informasjon om hvordan du definerer abonnementer, kan du se [Definere abonnementsgrupper](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="86f8e-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="86f8e-110">Når abonnementsgruppen er opprette, kan du opprette abonnementet.</span><span class="sxs-lookup"><span data-stu-id="86f8e-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="86f8e-111">Hvis du vil ha mer informasjon om hvordan du oppretter serviceabonnementer, kan du se [Opprette serviceabonnementer fra en abonnementsgruppe](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="86f8e-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="86f8e-112">Opprette og endre abonnementstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="86f8e-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="86f8e-113">Når du har definert abonnementet, oppretter du abonnementsavgiftstransaksjonen for den første faktureringsterminen, som er ett år.</span><span class="sxs-lookup"><span data-stu-id="86f8e-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="86f8e-114">Transaksjonene er av typen **Vanlig**.</span><span class="sxs-lookup"><span data-stu-id="86f8e-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="86f8e-115">Derfor kan du bare opprette abonnementstransaksjoner der fra-datoen og til-datoen tilsvarer periodene som tidligere ble opprettet i skjemae **Periodetyper**.</span><span class="sxs-lookup"><span data-stu-id="86f8e-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="86f8e-116">Hvis du vil ha mer informasjon om gebyrtransaksjoner, kan du se [Opprette abonnementsgebyrtransaksjoner](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="86f8e-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="86f8e-117">Når du har angitt abonnementet for kunden, husker du at de har forhandlet en 10 prosents rabatt på alle listeprisene for servicetilbudene.</span><span class="sxs-lookup"><span data-stu-id="86f8e-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="86f8e-118">Derfor må du redusere prisen for transaksjonsavgiften du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="86f8e-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="86f8e-119">Senere på dagen ringer kundekontakten for å si at selv om de fortsatt vil ha serviceavtalen for lysriggen, planlegger de å introdusere en ny lysrigg senere på året.</span><span class="sxs-lookup"><span data-stu-id="86f8e-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="86f8e-120">De trenger derfor bare vedlikeholdsdekning til oktober 2013.</span><span class="sxs-lookup"><span data-stu-id="86f8e-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="86f8e-121">For å redusere antall måneder i kundens abonnement oppretter du en ny abonnementutgiftstransaksjon av typen **Reduksjonsdager**.</span><span class="sxs-lookup"><span data-stu-id="86f8e-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="86f8e-122">Hvis du vil ha mer informasjon om hvordan du kan redusere dager, kan du se [Redusere dagene på abonnementsgebyr](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="86f8e-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="86f8e-123">Fakturere og avsette abonnementstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="86f8e-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="86f8e-124">Du har nå definert abonnementet, og du er klar til å fakturere kunden for det.</span><span class="sxs-lookup"><span data-stu-id="86f8e-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="86f8e-125">Hvis du vil ha mer informasjon om hvordan du fakturerer abonnementer, kan du se [Fakturere abonnementtransaksjoner](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="86f8e-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="86f8e-126">To dager senere ringer kunden for å si at abonnementet bør faktureres i amerikanske dollar, ikke euro.</span><span class="sxs-lookup"><span data-stu-id="86f8e-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="86f8e-127">Du oppretter derfor en kreditnota, og du oppretter også en ny abonnementstransaksjon i korrekt valuta.</span><span class="sxs-lookup"><span data-stu-id="86f8e-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="86f8e-128">Hvis du vil ha mer informasjon om hvordan du krediterer abonnementstransaksjoner, kan du se [Kreditere abonnementstransaksjoner](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="86f8e-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="86f8e-129">På slutten av hver måned kan én måneds inntekt avsettes fra kundens abonnement til resultatkontoen og VIA-kontoene.</span><span class="sxs-lookup"><span data-stu-id="86f8e-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="86f8e-130">Hvis du vil ha mer informasjon om hvordan du avsetter inntekt for abonnementer, kan du se [Avsette abonnementsomsetning](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="86f8e-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]