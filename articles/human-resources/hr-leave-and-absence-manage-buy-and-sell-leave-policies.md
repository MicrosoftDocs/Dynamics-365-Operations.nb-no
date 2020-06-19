---
title: Administrere policyer for kjøp og salg av permisjon
description: Du kan gjøre det mulig for ansatte å kjøpe og selge permisjon i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429019"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="47d99-103">Administrere policyer for kjøp og salg av permisjon</span><span class="sxs-lookup"><span data-stu-id="47d99-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="47d99-104">Du kan la de ansatte kjøpe permisjon ved å opprette en policy for å kjøpe permisjon.</span><span class="sxs-lookup"><span data-stu-id="47d99-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="47d99-105">Gjør det mulig for ansatte å kjøpe og selge permisjon</span><span class="sxs-lookup"><span data-stu-id="47d99-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="47d99-106">På **Parametere for permisjon og fravær**-siden velger du **Ja** for **Tillat ansatte å kjøpe permisjon**.</span><span class="sxs-lookup"><span data-stu-id="47d99-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="47d99-107">Opprette en policy for kjøp av permisjon</span><span class="sxs-lookup"><span data-stu-id="47d99-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="47d99-108">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="47d99-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="47d99-109">Velg **Policy for kjøp og salg av permisjon**.</span><span class="sxs-lookup"><span data-stu-id="47d99-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="47d99-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="47d99-110">Select **New**.</span></span>

4. <span data-ttu-id="47d99-111">Angi et **Navn** og en **Beskrivelse** for policyen under **Policy for kjøp og salg av permisjon**.</span><span class="sxs-lookup"><span data-stu-id="47d99-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="47d99-112">Velg en **Policytype**.</span><span class="sxs-lookup"><span data-stu-id="47d99-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="47d99-113">De tilgjengelige policytypene er **Antall** og **Timer per uke**.</span><span class="sxs-lookup"><span data-stu-id="47d99-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="47d99-114">Velg **Antall** for å angi et **Fast antall** for det maksimale antallet de ansatte kan kjøpe og selge.</span><span class="sxs-lookup"><span data-stu-id="47d99-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="47d99-115">Hvis du velger **Timer per uke**, brukes arbeidstiden som er definert i den ansattes tilordnede arbeidstidskalender, til å bestemme maksimumsantallet for policyen.</span><span class="sxs-lookup"><span data-stu-id="47d99-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="47d99-116">Velg en **Startdato** og **Sluttdato** for policyen.</span><span class="sxs-lookup"><span data-stu-id="47d99-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="47d99-117">Forespørsler om å kjøpe eller selge permisjon kan bare sendes innenfor denne tidsrammen.</span><span class="sxs-lookup"><span data-stu-id="47d99-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="47d99-118">Under **Kjøpspolicy** velger du **Fulltidsekvivalent** (fte) for å fordele maksimumsantallet proporsjonalt på grunnlag av fulltidsekvivalenten som er definert i den ansattes stilling.</span><span class="sxs-lookup"><span data-stu-id="47d99-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="47d99-119">Hvis policytypen er **Antall**, angir du et **Maksimalt fastsatt antall**.</span><span class="sxs-lookup"><span data-stu-id="47d99-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="47d99-120">Velg **Legg til** for å legge til permisjonstyper for ansatte som vil kjøpe permisjon.</span><span class="sxs-lookup"><span data-stu-id="47d99-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="47d99-121">Du kan legge til flere permisjonstyper i policyen.</span><span class="sxs-lookup"><span data-stu-id="47d99-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="47d99-122">Angi **Måneder med jobberfaring** som permisjonstype for å aktivere forskjellige måneder med jobberfaring og fastslå det maksimale antallet en ansatt kan kjøpe.</span><span class="sxs-lookup"><span data-stu-id="47d99-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="47d99-123">Angi **Maksimalt antall** for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="47d99-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="47d99-124">Angi en **Sats** som den ansatte kan kjøpe permisjon til.</span><span class="sxs-lookup"><span data-stu-id="47d99-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="47d99-125">Du kan eventuelt angi en **Inntektskode** som kan brukes til å kjøpe permisjon.</span><span class="sxs-lookup"><span data-stu-id="47d99-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="47d99-126">Angi eventuelt om du vil bruke FTE til å bestemme det maksimale antallet for permisjonstypen.</span><span class="sxs-lookup"><span data-stu-id="47d99-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="47d99-127">Legge til policyen for kjøp og salg av permisjon i en permisjons- og fraværsplan</span><span class="sxs-lookup"><span data-stu-id="47d99-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="47d99-128">På **Permisjon og fravær**-siden velger du en permisjons- og fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="47d99-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="47d99-129">Under **Regler** velger du **Policy for kjøp og salg av permisjon**.</span><span class="sxs-lookup"><span data-stu-id="47d99-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="47d99-130">Se også</span><span class="sxs-lookup"><span data-stu-id="47d99-130">See also</span></span>

[<span data-ttu-id="47d99-131">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="47d99-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="47d99-132">Konfigurere permisjons- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="47d99-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="47d99-133">Avsett permisjons- og fraværsplaner</span><span class="sxs-lookup"><span data-stu-id="47d99-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="47d99-134">Kjøp og selg permisjon</span><span class="sxs-lookup"><span data-stu-id="47d99-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

