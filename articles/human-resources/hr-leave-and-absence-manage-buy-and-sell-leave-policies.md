---
title: Administrere policyer for kjøp og salg av permisjon
description: Du kan gjøre det mulig for ansatte å kjøpe og selge permisjon i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f03d6055c407b2c3e13831c8b5a6f8b0d6c47897
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794715"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="d17a5-103">Administrere policyer for kjøp og salg av permisjon</span><span class="sxs-lookup"><span data-stu-id="d17a5-103">Manage buy and sell leave policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d17a5-104">Du kan la de ansatte kjøpe og selge permisjon ved å opprette en policy for å kjøpe og selge permisjon.</span><span class="sxs-lookup"><span data-stu-id="d17a5-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="d17a5-105">Du kan konfigurere disse policyene til å bruke arbeidsflyt for godkjenninger, angi maksimumsbeløp og -satser og angi satser for kjøp og salg.</span><span class="sxs-lookup"><span data-stu-id="d17a5-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="d17a5-106">Gjør det mulig for ansatte å kjøpe og selge permisjon</span><span class="sxs-lookup"><span data-stu-id="d17a5-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="d17a5-107">På **Parametere for permisjon og fravær**-siden velger du **Ja** for **Tillat ansatte å kjøpe permisjon** og **Tillat ansatte å selge permisjon**.</span><span class="sxs-lookup"><span data-stu-id="d17a5-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="d17a5-108">Opprette en policy for kjøp og salg av permisjon</span><span class="sxs-lookup"><span data-stu-id="d17a5-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="d17a5-109">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="d17a5-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="d17a5-110">Velg **Policy for kjøp og salg av permisjon**.</span><span class="sxs-lookup"><span data-stu-id="d17a5-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="d17a5-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d17a5-111">Select **New**.</span></span>

4. <span data-ttu-id="d17a5-112">Angi et **Navn** og en **Beskrivelse** for policyen under **Policy for kjøp og salg av permisjon**.</span><span class="sxs-lookup"><span data-stu-id="d17a5-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="d17a5-113">Velg en **Policytype**.</span><span class="sxs-lookup"><span data-stu-id="d17a5-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="d17a5-114">De tilgjengelige policytypene er **Antall** og **Timer per uke**.</span><span class="sxs-lookup"><span data-stu-id="d17a5-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="d17a5-115">Velg **Antall** for å angi et **Fast antall** for det maksimale antallet de ansatte kan kjøpe og selge.</span><span class="sxs-lookup"><span data-stu-id="d17a5-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="d17a5-116">Hvis du velger **Timer per uke**, brukes arbeidstiden som er definert i den ansattes tilordnede arbeidstidskalender, til å bestemme maksimumsantallet for policyen.</span><span class="sxs-lookup"><span data-stu-id="d17a5-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="d17a5-117">Velg en **Startdato** og **Sluttdato** for policyen.</span><span class="sxs-lookup"><span data-stu-id="d17a5-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="d17a5-118">Forespørsler om å kjøpe eller selge permisjon kan bare sendes innenfor denne tidsrammen.</span><span class="sxs-lookup"><span data-stu-id="d17a5-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="d17a5-119">Velg en **Arbeidsflyt-ID** for policyen.</span><span class="sxs-lookup"><span data-stu-id="d17a5-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="d17a5-120">Alle kjøps- og salgsforespørsler vil bruke denne arbeidsflyten til gjennomgang og godkjenning.</span><span class="sxs-lookup"><span data-stu-id="d17a5-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="d17a5-121">Under **Kjøpspolicy** velger du **Fulltidsekvivalent** (fte) for å fordele maksimumsantallet proporsjonalt på grunnlag av fulltidsekvivalenten som er definert i den ansattes stilling.</span><span class="sxs-lookup"><span data-stu-id="d17a5-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="d17a5-122">Hvis policytypen er **Antall**, angir du et **Maksimalt fastsatt antall**.</span><span class="sxs-lookup"><span data-stu-id="d17a5-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="d17a5-123">Velg **Legg til** for å legge til permisjonstyper for ansatte som vil kjøpe permisjon.</span><span class="sxs-lookup"><span data-stu-id="d17a5-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="d17a5-124">Du kan legge til flere permisjonstyper i policyen.</span><span class="sxs-lookup"><span data-stu-id="d17a5-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="d17a5-125">Angi **Måneder med jobberfaring** som permisjonstype for å aktivere forskjellige måneder med jobberfaring og fastslå det maksimale antallet en ansatt kan kjøpe.</span><span class="sxs-lookup"><span data-stu-id="d17a5-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="d17a5-126">Angi **Maksimalt antall** for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="d17a5-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="d17a5-127">Angi en **Sats** som den ansatte kan kjøpe permisjon til.</span><span class="sxs-lookup"><span data-stu-id="d17a5-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="d17a5-128">Du kan eventuelt angi en **Inntektskode** som kan brukes til å kjøpe permisjon.</span><span class="sxs-lookup"><span data-stu-id="d17a5-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="d17a5-129">Angi eventuelt om du vil bruke FTE til å bestemme det maksimale antallet for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="d17a5-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="d17a5-130">Hvis du vil opprette en salgspolicy, følger du trinn 8 til 14 under **Salgspolicy**.</span><span class="sxs-lookup"><span data-stu-id="d17a5-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="d17a5-131">Legge til policyen for kjøp og salg av permisjon i en permisjons- og fraværsplan</span><span class="sxs-lookup"><span data-stu-id="d17a5-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="d17a5-132">På **Permisjon og fravær**-siden velger du en permisjons- og fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="d17a5-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="d17a5-133">Under **Regler** velger du **Policy for kjøp og salg av permisjon**.</span><span class="sxs-lookup"><span data-stu-id="d17a5-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d17a5-134">Se også</span><span class="sxs-lookup"><span data-stu-id="d17a5-134">See also</span></span>

[<span data-ttu-id="d17a5-135">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="d17a5-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="d17a5-136">Konfigurere permisjons- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="d17a5-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="d17a5-137">Avsett permisjons- og fraværsplaner</span><span class="sxs-lookup"><span data-stu-id="d17a5-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="d17a5-138">Kjøp og selg permisjon</span><span class="sxs-lookup"><span data-stu-id="d17a5-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]