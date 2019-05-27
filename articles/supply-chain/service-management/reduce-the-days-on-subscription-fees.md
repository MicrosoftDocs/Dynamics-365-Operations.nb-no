---
title: Redusere dagene på abonnementsgebyr
description: Hvis du vil redusere antall dager for en eksisterende abonnementsavgift, kan du opprette en ny transaksjon der du fjerner tidsperioden som ikke lenger skal være del av abonnementsavgiftsintervallet.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04b183d8fc8083c630bcb4e0e69fb755f8a50f95
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569736"
---
# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="75148-103">Redusere dagene på abonnementsgebyr</span><span class="sxs-lookup"><span data-stu-id="75148-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="75148-104">Hvis du vil redusere antall dager for en eksisterende abonnementsavgift, kan du opprette en ny transaksjon der du fjerner tidsperioden som ikke lenger skal være del av abonnementsavgiftsintervallet.</span><span class="sxs-lookup"><span data-stu-id="75148-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="75148-105">Redusere dager på en abonnementsavgift</span><span class="sxs-lookup"><span data-stu-id="75148-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="75148-106">Klikk på **Servicestyring** \> **Felles** \> **Serviceabonnementer** \> **Alle serviceabonnementer**.</span><span class="sxs-lookup"><span data-stu-id="75148-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="75148-107">Velg serviceabonnementet, og klikk **Abonnementsavgifter** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="75148-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="75148-108">I feltet **Abonnementstype** velger du **Reduksjonsdager**.</span><span class="sxs-lookup"><span data-stu-id="75148-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="75148-109">Bruk feltet **Fra dato** og feltet **Til dato** til å definere datointervallet for abonnementsavgiften du vil fjerne fra abonnementsavgiftsperioden, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="75148-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="75148-110">Hvis du vil vise transaksjonene som ble opprettet, i skjemaet **Abonnement**, klikker du **Gebyrtransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="75148-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="75148-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="75148-111">Example</span></span>

<span data-ttu-id="75148-112">Hvis en periode for abonnementstransaksjon går fra 1. januar til 31. januar, og du vil redusere perioden med 10 dager, oppretter du en ny transaksjon der perioden er 1. januar til 10. januar.</span><span class="sxs-lookup"><span data-stu-id="75148-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="75148-113">(Reduksjonsperioden kan også være 5. januar til 15. januar eller en vilkårlig periode på ti dager.)</span><span class="sxs-lookup"><span data-stu-id="75148-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="75148-114">I tillegg hvis **Fra dato** i reduksjonsperioden er 21. januar (31 minus 10), kan du angi **Til dato** til en hvilken som helst dato etter 31. januar, og det fjernes automatisk 10 dager fra avgiftstransaksjonsperioden.</span><span class="sxs-lookup"><span data-stu-id="75148-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="75148-115">Se også</span><span class="sxs-lookup"><span data-stu-id="75148-115">See also</span></span>

[<span data-ttu-id="75148-116">Reduksjonsdager – eksempel</span><span class="sxs-lookup"><span data-stu-id="75148-116">Reduction days example</span></span>](reduction-days-example.md)

  


