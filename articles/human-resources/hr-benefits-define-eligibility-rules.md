---
title: Definere rettighetsregler og policyer for fordel
description: Denne artikkelen viser deg hvordan du kan opprette rettighetsregler og policyer for fordel og deretter tilordne regler til fordeler.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 046b045fbdda125c5a2259783c0347f687453528
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053159"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="42c38-103">Definere rettighetsregler og policyer for fordel</span><span class="sxs-lookup"><span data-stu-id="42c38-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="42c38-104">Dette emnet viser hvordan du kan opprette rettighetsregler og policyer for fordeler og deretter tilordne regler til fordeler.</span><span class="sxs-lookup"><span data-stu-id="42c38-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="42c38-105">Opprette policyregeltype for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="42c38-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="42c38-106">Gå til **Human resources > Fordeler > Rettighet > Policyregeltyper for fordelsrettigheter**.</span><span class="sxs-lookup"><span data-stu-id="42c38-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="42c38-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="42c38-107">Select **New**.</span></span>
3. <span data-ttu-id="42c38-108">Angi en verdi i feltet **Regelnavn**.</span><span class="sxs-lookup"><span data-stu-id="42c38-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="42c38-109">Angi en verdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="42c38-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="42c38-110">I feltet **Spørringsnavn** velger du rullegardinknappen for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="42c38-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="42c38-111">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="42c38-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="42c38-112">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="42c38-112">Select **Save**.</span></span>
8. <span data-ttu-id="42c38-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="42c38-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="42c38-114">Policy for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="42c38-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="42c38-115">Gå til **Human resources > Fordeler > Rettighet > Policyer for fordelsrettigheter**.</span><span class="sxs-lookup"><span data-stu-id="42c38-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="42c38-116">Velg en eksisterende fordelspolicy.</span><span class="sxs-lookup"><span data-stu-id="42c38-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="42c38-117">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="42c38-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="42c38-118">Aktiver/deaktiver utvidelsen av delen **Policyorganisasjoner**.</span><span class="sxs-lookup"><span data-stu-id="42c38-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="42c38-119">Du kan legge til eller fjerne alle organisasjoner som du vil ta med i policyen.</span><span class="sxs-lookup"><span data-stu-id="42c38-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="42c38-120">Vis eller skjul delen **Policyregler**.</span><span class="sxs-lookup"><span data-stu-id="42c38-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="42c38-121">I listen finner du policyregelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="42c38-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="42c38-122">Velg **Opprett policyregel**.</span><span class="sxs-lookup"><span data-stu-id="42c38-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="42c38-123">I feltet **Gjelder fra** angir du datoen du vil at policyen skal aktiveres.</span><span class="sxs-lookup"><span data-stu-id="42c38-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="42c38-124">Ved å angi effektive sluttdatoer kan du endre fremtidige policyregler, slik at du ikke må gå tilbake til policyen når du vil at endringene skal tre i kraft.</span><span class="sxs-lookup"><span data-stu-id="42c38-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="42c38-125">Om nødvendig legger du til et where-uttrykk i feltet **Legg til betingelse**.</span><span class="sxs-lookup"><span data-stu-id="42c38-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="42c38-126">Hvis du for eksempel vil at regelen bare skal gjelde for salgssjefer, kan du opprette Where-uttrykket for å si: der stillingsbeskrivelsen er lik Salgssjef.</span><span class="sxs-lookup"><span data-stu-id="42c38-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="42c38-127">Du kan legge til flere where-uttrykk sammen i en regel.</span><span class="sxs-lookup"><span data-stu-id="42c38-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="42c38-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="42c38-128">Select **OK**.</span></span>
11. <span data-ttu-id="42c38-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="42c38-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="42c38-130">Tilordne regel til fordel</span><span class="sxs-lookup"><span data-stu-id="42c38-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="42c38-131">Gå til **Human resources > Fordeler > Fordeler**.</span><span class="sxs-lookup"><span data-stu-id="42c38-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="42c38-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="42c38-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="42c38-133">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="42c38-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="42c38-134">Vis eller skjul delen **Rettighetsregler**.</span><span class="sxs-lookup"><span data-stu-id="42c38-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="42c38-135">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="42c38-135">Select **Edit**.</span></span>
6. <span data-ttu-id="42c38-136">Velg regelen i **Rettighet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="42c38-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="42c38-137">I feltet **Regeltype** velger du regelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="42c38-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="42c38-138">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="42c38-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="42c38-139">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="42c38-139">Select **Save**.</span></span>
11. <span data-ttu-id="42c38-140">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="42c38-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]