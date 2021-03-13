---
title: Definere rettighetsregler og policyer for fordel
description: Denne artikkelen viser deg hvordan du kan opprette rettighetsregler og policyer for fordel og deretter tilordne regler til fordeler.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: cc80549eaffa72a22dec51829c86d04a763de96a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113673"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="32def-103">Definere rettighetsregler og policyer for fordel</span><span class="sxs-lookup"><span data-stu-id="32def-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="32def-104">Dette emnet viser hvordan du kan opprette rettighetsregler og policyer for fordeler og deretter tilordne regler til fordeler.</span><span class="sxs-lookup"><span data-stu-id="32def-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="32def-105">Opprette policyregeltype for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="32def-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="32def-106">Gå til **Human resources > Fordeler > Rettighet > Policyregeltyper for fordelsrettigheter**.</span><span class="sxs-lookup"><span data-stu-id="32def-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="32def-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="32def-107">Select **New**.</span></span>
3. <span data-ttu-id="32def-108">Angi en verdi i feltet **Regelnavn**.</span><span class="sxs-lookup"><span data-stu-id="32def-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="32def-109">Angi en verdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="32def-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="32def-110">I feltet **Spørringsnavn** velger du rullegardinknappen for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="32def-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="32def-111">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32def-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="32def-112">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="32def-112">Select **Save**.</span></span>
8. <span data-ttu-id="32def-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="32def-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="32def-114">Policy for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="32def-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="32def-115">Gå til **Human resources > Fordeler > Rettighet > Policyer for fordelsrettigheter**.</span><span class="sxs-lookup"><span data-stu-id="32def-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="32def-116">Velg en eksisterende fordelspolicy.</span><span class="sxs-lookup"><span data-stu-id="32def-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="32def-117">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32def-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="32def-118">Aktiver/deaktiver utvidelsen av delen **Policyorganisasjoner**.</span><span class="sxs-lookup"><span data-stu-id="32def-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="32def-119">Du kan legge til eller fjerne alle organisasjoner som du vil ta med i policyen.</span><span class="sxs-lookup"><span data-stu-id="32def-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="32def-120">Vis eller skjul delen **Policyregler**.</span><span class="sxs-lookup"><span data-stu-id="32def-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="32def-121">I listen finner du policyregelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="32def-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="32def-122">Velg **Opprett policyregel**.</span><span class="sxs-lookup"><span data-stu-id="32def-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="32def-123">I feltet **Gjelder fra** angir du datoen du vil at policyen skal aktiveres.</span><span class="sxs-lookup"><span data-stu-id="32def-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="32def-124">Ved å angi effektive sluttdatoer kan du endre fremtidige policyregler, slik at du ikke må gå tilbake til policyen når du vil at endringene skal tre i kraft.</span><span class="sxs-lookup"><span data-stu-id="32def-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="32def-125">Om nødvendig legger du til et where-uttrykk i feltet **Legg til betingelse**.</span><span class="sxs-lookup"><span data-stu-id="32def-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="32def-126">Hvis du for eksempel vil at regelen bare skal gjelde for salgssjefer, kan du opprette Where-uttrykket for å si: der stillingsbeskrivelsen er lik Salgssjef.</span><span class="sxs-lookup"><span data-stu-id="32def-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="32def-127">Du kan legge til flere where-uttrykk sammen i en regel.</span><span class="sxs-lookup"><span data-stu-id="32def-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="32def-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="32def-128">Select **OK**.</span></span>
11. <span data-ttu-id="32def-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="32def-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="32def-130">Tilordne regel til fordel</span><span class="sxs-lookup"><span data-stu-id="32def-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="32def-131">Gå til **Human resources > Fordeler > Fordeler**.</span><span class="sxs-lookup"><span data-stu-id="32def-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="32def-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="32def-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="32def-133">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32def-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="32def-134">Vis eller skjul delen **Rettighetsregler**.</span><span class="sxs-lookup"><span data-stu-id="32def-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="32def-135">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="32def-135">Select **Edit**.</span></span>
6. <span data-ttu-id="32def-136">Velg regelen i **Rettighet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="32def-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="32def-137">I feltet **Regeltype** velger du regelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="32def-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="32def-138">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32def-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="32def-139">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="32def-139">Select **Save**.</span></span>
11. <span data-ttu-id="32def-140">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="32def-140">Close the form.</span></span>

