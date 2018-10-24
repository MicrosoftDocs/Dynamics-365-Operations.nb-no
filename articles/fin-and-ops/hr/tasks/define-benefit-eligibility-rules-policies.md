--- 
title: Definere rettighetsregler og policyer for fordel
description: Denne registreringen viser deg hvordan du kan opprette rettighetsregler og policyer for fordel og deretter tilordne regler til fordeler.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d346c3277e8f19020d6aa96cf6961c4c52ac28fb
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="2449b-103">Definere rettighetsregler og policyer for fordel</span><span class="sxs-lookup"><span data-stu-id="2449b-103">Define benefit eligibility rules and policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2449b-104">Denne registreringen viser deg hvordan du kan opprette rettighetsregler og policyer for fordel og deretter tilordne regler til fordeler.</span><span class="sxs-lookup"><span data-stu-id="2449b-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="2449b-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette dette opptaket.</span><span class="sxs-lookup"><span data-stu-id="2449b-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="2449b-106">Opprette policyregeltype for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="2449b-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="2449b-107">Gå til Personale > Fordeler > Rettighet > Policyregeltyper for fordelsrettigheter.</span><span class="sxs-lookup"><span data-stu-id="2449b-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="2449b-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2449b-108">Click New.</span></span>
3. <span data-ttu-id="2449b-109">Skriv inn en verdi i feltet Regelnavn.</span><span class="sxs-lookup"><span data-stu-id="2449b-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="2449b-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2449b-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2449b-111">Klikk rullegardinknappen i Spørringsnavn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="2449b-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2449b-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2449b-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2449b-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="2449b-113">Click Save.</span></span>
8. <span data-ttu-id="2449b-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2449b-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="2449b-115">Policy for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="2449b-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="2449b-116">Gå til Personale > Fordeler > Rettighet > Policyer for fordelsrettigheter.</span><span class="sxs-lookup"><span data-stu-id="2449b-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="2449b-117">Velg en eksisterende fordelspolicy.</span><span class="sxs-lookup"><span data-stu-id="2449b-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="2449b-118">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2449b-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2449b-119">Aktiver/deaktiver utvidelsen av delen Policyorganisasjoner.</span><span class="sxs-lookup"><span data-stu-id="2449b-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="2449b-120">Her kan du legge til eller fjerne alle organisasjoner som du vil ta med i policyen.</span><span class="sxs-lookup"><span data-stu-id="2449b-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="2449b-121">Vis eller skjul delen Policyregler.</span><span class="sxs-lookup"><span data-stu-id="2449b-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="2449b-122">I listen finner du policyregelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="2449b-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="2449b-123">Klikk Opprett policyregel.</span><span class="sxs-lookup"><span data-stu-id="2449b-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="2449b-124">I feltet Gjelder fra angir du datoen du vil at policyen skal aktiveres.</span><span class="sxs-lookup"><span data-stu-id="2449b-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="2449b-125">Ved å angi effektive datoer og sluttdatoer kan du endre fremtidige policyregler og fjerne behovet for å gå tilbake til policyen når du vil at endringene skal tre i kraft.</span><span class="sxs-lookup"><span data-stu-id="2449b-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="2449b-126">Hvis du for eksempel vil at regelen bare skal gjelde for salgssjefer, kan du opprette Where-uttrykket for å si: der stillingsbeskrivelsen er lik Salgssjef.</span><span class="sxs-lookup"><span data-stu-id="2449b-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="2449b-127">Du kan bruke And eller Or og flere Where-uttrykk sammen i regelen.</span><span class="sxs-lookup"><span data-stu-id="2449b-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="2449b-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2449b-128">Click OK.</span></span>
11. <span data-ttu-id="2449b-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2449b-129">Close the page.</span></span>
12. <span data-ttu-id="2449b-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2449b-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="2449b-131">Tilordne regel til fordel</span><span class="sxs-lookup"><span data-stu-id="2449b-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="2449b-132">Gå til Personale > Fordeler > Fordeler.</span><span class="sxs-lookup"><span data-stu-id="2449b-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="2449b-133">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2449b-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2449b-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2449b-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2449b-135">Vis eller skjul delen Rettighetsregler.</span><span class="sxs-lookup"><span data-stu-id="2449b-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="2449b-136">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="2449b-136">Click Edit.</span></span>
6. <span data-ttu-id="2449b-137">Velg Regelbasert fra listen i Rettighet-feltet.</span><span class="sxs-lookup"><span data-stu-id="2449b-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="2449b-138">Klikk rullegardinknappen i Regeltype-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="2449b-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="2449b-139">I listen finner og velger du regelen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="2449b-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="2449b-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2449b-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="2449b-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="2449b-141">Click Save.</span></span>
11. <span data-ttu-id="2449b-142">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="2449b-142">Close the form.</span></span>


