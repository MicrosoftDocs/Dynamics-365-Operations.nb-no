---
title: Konfigurere alternativer for personlige kontaktrettigheter
description: Konfigurer rettighetsalternativer for personlige kontakter i Microsoft Dynamics 365 Human Resources. Personlige kontakter kan være mottakere eller avhengige.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f300ac917ac21db9fffbffcc6eb8589357c0a3e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466212"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="dff37-104">Konfigurere alternativer for personlige kontaktrettigheter</span><span class="sxs-lookup"><span data-stu-id="dff37-104">Configure personal contact eligibility options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dff37-105">I denne artikkelen får du vite hvordan du konfigurerer typer personlige kontakter som skal brukes i fordeler i Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dff37-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="dff37-106">Personlige kontakter kan være mottakere eller avhengige.</span><span class="sxs-lookup"><span data-stu-id="dff37-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="dff37-107">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Alternativer for rettighet for personlig kontakt**.</span><span class="sxs-lookup"><span data-stu-id="dff37-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="dff37-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dff37-108">Select **New**.</span></span>

3. <span data-ttu-id="dff37-109">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="dff37-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="dff37-110">Felt</span><span class="sxs-lookup"><span data-stu-id="dff37-110">Field</span></span> | <span data-ttu-id="dff37-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="dff37-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="dff37-112">**Rettighetsalternativ**</span><span class="sxs-lookup"><span data-stu-id="dff37-112">**Eligibility option**</span></span> | <span data-ttu-id="dff37-113">Et unikt navn på et rettighetsalternativ eller en kode som identifiserer rettighetsalternativet.</span><span class="sxs-lookup"><span data-stu-id="dff37-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="dff37-114">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="dff37-114">**Description**</span></span> | <span data-ttu-id="dff37-115">En kort beskrivelse av rettighetsalternativet.</span><span class="sxs-lookup"><span data-stu-id="dff37-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="dff37-116">**Rettighetskode for kontakt**</span><span class="sxs-lookup"><span data-stu-id="dff37-116">**Contact eligibility code**</span></span> | <span data-ttu-id="dff37-117">Systemkoden som best beskriver det personlige rettighetsalternativet.</span><span class="sxs-lookup"><span data-stu-id="dff37-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="dff37-118">Du kan velge blant:</span><span class="sxs-lookup"><span data-stu-id="dff37-118">You can choose from:</span></span> <ul><li><span data-ttu-id="dff37-119">Relasjon</span><span class="sxs-lookup"><span data-stu-id="dff37-119">Relationship</span></span></li><li><span data-ttu-id="dff37-120">Student</span><span class="sxs-lookup"><span data-stu-id="dff37-120">Student</span></span></li><li><span data-ttu-id="dff37-121">Overårig avhengig</span><span class="sxs-lookup"><span data-stu-id="dff37-121">Overage dependent</span></span></li><li><span data-ttu-id="dff37-122">Overårig avhengig som er ufør</span><span class="sxs-lookup"><span data-stu-id="dff37-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="dff37-123">**Status**</span><span class="sxs-lookup"><span data-stu-id="dff37-123">**Status**</span></span> | <span data-ttu-id="dff37-124">Statusen for rettighetsalternativet.</span><span class="sxs-lookup"><span data-stu-id="dff37-124">The status of the eligibility option.</span></span> <span data-ttu-id="dff37-125">Hvis statusen for et rettighetsalternativ er satt til Inaktiv, kan du ikke velge dette rettighetsalternativet for personlige kontakter.</span><span class="sxs-lookup"><span data-stu-id="dff37-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="dff37-126">**Relasjon**</span><span class="sxs-lookup"><span data-stu-id="dff37-126">**Relationship**</span></span> | <span data-ttu-id="dff37-127">Angir relasjonen mellom den personlige kontakten og den ansatte.</span><span class="sxs-lookup"><span data-stu-id="dff37-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="dff37-128">Dette feltet er bare aktivt hvis kontaktrettighetskoden er satt til Relasjon.</span><span class="sxs-lookup"><span data-stu-id="dff37-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="dff37-129">**Alder**</span><span class="sxs-lookup"><span data-stu-id="dff37-129">**Age**</span></span> | <span data-ttu-id="dff37-130">Maksimal alder på en personlig kontakt for fordelsplanen.</span><span class="sxs-lookup"><span data-stu-id="dff37-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="dff37-131">Dette feltet er bare aktivt hvis du velger en relasjon.</span><span class="sxs-lookup"><span data-stu-id="dff37-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="dff37-132">Denne alderen sammenlignes med den beregnede alderen på den personlige kontakten.</span><span class="sxs-lookup"><span data-stu-id="dff37-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="dff37-133">Beregnet alder er: (dekningsdato – fødselsdato for personlig kontakt / 365).</span><span class="sxs-lookup"><span data-stu-id="dff37-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="dff37-134">Dette tallet er alltid et heltall.</span><span class="sxs-lookup"><span data-stu-id="dff37-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="dff37-135">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dff37-135">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]