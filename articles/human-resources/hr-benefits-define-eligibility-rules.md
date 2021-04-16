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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: df517e1ab72634cb434411fab3bd92bf34c7e609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805952"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="17a2c-103">Definere rettighetsregler og policyer for fordel</span><span class="sxs-lookup"><span data-stu-id="17a2c-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="17a2c-104">Dette emnet viser hvordan du kan opprette rettighetsregler og policyer for fordeler og deretter tilordne regler til fordeler.</span><span class="sxs-lookup"><span data-stu-id="17a2c-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="17a2c-105">Opprette policyregeltype for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="17a2c-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="17a2c-106">Gå til **Human resources > Fordeler > Rettighet > Policyregeltyper for fordelsrettigheter**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="17a2c-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-107">Select **New**.</span></span>
3. <span data-ttu-id="17a2c-108">Angi en verdi i feltet **Regelnavn**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="17a2c-109">Angi en verdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="17a2c-110">I feltet **Spørringsnavn** velger du rullegardinknappen for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="17a2c-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="17a2c-111">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="17a2c-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="17a2c-112">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-112">Select **Save**.</span></span>
8. <span data-ttu-id="17a2c-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="17a2c-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="17a2c-114">Policy for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="17a2c-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="17a2c-115">Gå til **Human resources > Fordeler > Rettighet > Policyer for fordelsrettigheter**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="17a2c-116">Velg en eksisterende fordelspolicy.</span><span class="sxs-lookup"><span data-stu-id="17a2c-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="17a2c-117">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="17a2c-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="17a2c-118">Aktiver/deaktiver utvidelsen av delen **Policyorganisasjoner**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="17a2c-119">Du kan legge til eller fjerne alle organisasjoner som du vil ta med i policyen.</span><span class="sxs-lookup"><span data-stu-id="17a2c-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="17a2c-120">Vis eller skjul delen **Policyregler**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="17a2c-121">I listen finner du policyregelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="17a2c-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="17a2c-122">Velg **Opprett policyregel**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="17a2c-123">I feltet **Gjelder fra** angir du datoen du vil at policyen skal aktiveres.</span><span class="sxs-lookup"><span data-stu-id="17a2c-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="17a2c-124">Ved å angi effektive sluttdatoer kan du endre fremtidige policyregler, slik at du ikke må gå tilbake til policyen når du vil at endringene skal tre i kraft.</span><span class="sxs-lookup"><span data-stu-id="17a2c-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="17a2c-125">Om nødvendig legger du til et where-uttrykk i feltet **Legg til betingelse**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="17a2c-126">Hvis du for eksempel vil at regelen bare skal gjelde for salgssjefer, kan du opprette Where-uttrykket for å si: der stillingsbeskrivelsen er lik Salgssjef.</span><span class="sxs-lookup"><span data-stu-id="17a2c-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="17a2c-127">Du kan legge til flere where-uttrykk sammen i en regel.</span><span class="sxs-lookup"><span data-stu-id="17a2c-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="17a2c-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-128">Select **OK**.</span></span>
11. <span data-ttu-id="17a2c-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="17a2c-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="17a2c-130">Tilordne regel til fordel</span><span class="sxs-lookup"><span data-stu-id="17a2c-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="17a2c-131">Gå til **Human resources > Fordeler > Fordeler**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="17a2c-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="17a2c-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="17a2c-133">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="17a2c-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="17a2c-134">Vis eller skjul delen **Rettighetsregler**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="17a2c-135">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-135">Select **Edit**.</span></span>
6. <span data-ttu-id="17a2c-136">Velg regelen i **Rettighet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="17a2c-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="17a2c-137">I feltet **Regeltype** velger du regelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="17a2c-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="17a2c-138">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="17a2c-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="17a2c-139">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="17a2c-139">Select **Save**.</span></span>
11. <span data-ttu-id="17a2c-140">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="17a2c-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]