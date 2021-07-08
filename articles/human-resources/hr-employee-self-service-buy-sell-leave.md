---
title: Kjøp og selg permisjon
description: I Dynamics 365 Human Resources kan du sende forespørsler om å kjøpe og selge permisjon basert på retningslinjene for kjøp og salg som er satt opp av firmaet.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271497"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="b6177-103">Kjøp og selg permisjon</span><span class="sxs-lookup"><span data-stu-id="b6177-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b6177-104">I Dynamics 365 Human Resources kan du sende forespørsler om å kjøpe og selge permisjon basert på retningslinjene for kjøp og salg som er satt opp av firmaet.</span><span class="sxs-lookup"><span data-stu-id="b6177-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="b6177-105">Forespørsel om å kjøpe permisjon</span><span class="sxs-lookup"><span data-stu-id="b6177-105">Request to buy leave</span></span>

1. <span data-ttu-id="b6177-106">I arbeidsområdet **Ansattselvbetjening** velger du **Forespørsel om å kjøpe permisjon** på flisen **Avspaseringssaldoer**.</span><span class="sxs-lookup"><span data-stu-id="b6177-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="b6177-107">Legg til en **Permisjonstype**, og angi et **Antall** som indikerer hvor mye permisjon du vil kjøpe.</span><span class="sxs-lookup"><span data-stu-id="b6177-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="b6177-108">Velg **Send inn** når du er klar til å sende inn forespørselen.</span><span class="sxs-lookup"><span data-stu-id="b6177-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="b6177-109">Saldoene blir enten automatisk oppdaterte eller går gjennom en godkjenningsprosess før oppdatering.</span><span class="sxs-lookup"><span data-stu-id="b6177-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="b6177-110">Dette avhenger av hvordan kjøpspolicyen er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="b6177-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="b6177-111">Forespørsel om å selge permisjon</span><span class="sxs-lookup"><span data-stu-id="b6177-111">Request to sell leave</span></span>

1. <span data-ttu-id="b6177-112">I arbeidsområdet **Ansattselvbetjening** velger du **Forespørsel om å selge permisjon** på flisen **Avspaseringssaldoer**.</span><span class="sxs-lookup"><span data-stu-id="b6177-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="b6177-113">Legg til en **Permisjonstype**, og angi et **Antall** som indikerer hvor mye permisjon du vil selge.</span><span class="sxs-lookup"><span data-stu-id="b6177-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="b6177-114">Velg **Send inn** når du er klar til å sende inn forespørselen.</span><span class="sxs-lookup"><span data-stu-id="b6177-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="b6177-115">Saldoene blir enten automatisk oppdaterte eller går gjennom en godkjenningsprosess før oppdatering.</span><span class="sxs-lookup"><span data-stu-id="b6177-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="b6177-116">Dette avhenger av hvordan kjøpspolicyen er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="b6177-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="b6177-117">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="b6177-117">Troubleshooting</span></span> 

<span data-ttu-id="b6177-118">Hvis arbeidsflyten for kjøp eller salg av permisjonsforespørsel mislykkes, kan brukere med rettigheten **EssLeaveBuySellRequestApprover** se gjennom meldingsloggen for alle forespørsler om kjøp og salg av permisjon.</span><span class="sxs-lookup"><span data-stu-id="b6177-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="b6177-119">Hvis du vil gjøre dette, kan du gå til **Permisjon og fravær > Kobling > Forepørsel om kjøp og salg av permisjon > Meldingslogg** (øverst til venstre).</span><span class="sxs-lookup"><span data-stu-id="b6177-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="b6177-120">**Meldingsloggen** viser brukere hvordan transaksjonene ble behandlet og den tilknyttede arbeidsflytloggen.</span><span class="sxs-lookup"><span data-stu-id="b6177-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="b6177-121">Se også</span><span class="sxs-lookup"><span data-stu-id="b6177-121">See also</span></span>

[<span data-ttu-id="b6177-122">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="b6177-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="b6177-123">Administrere policyer for kjøp og salg av permisjon</span><span class="sxs-lookup"><span data-stu-id="b6177-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
