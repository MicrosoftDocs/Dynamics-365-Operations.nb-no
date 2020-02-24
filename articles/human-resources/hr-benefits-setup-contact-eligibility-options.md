---
title: Konfigurere alternativer for personlige kontaktrettigheter
description: Konfigurer rettighetsalternativer for personlige kontakter i Microsoft Dynamics 365 Human Resources. Personlige kontakter kan være mottakere eller avhengige.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010093"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="28d59-104">Konfigurere alternativer for personlige kontaktrettigheter</span><span class="sxs-lookup"><span data-stu-id="28d59-104">Configure personal contact eligibility options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="28d59-105">I denne artikkelen får du vite hvordan du konfigurerer typer personlige kontakter som skal brukes i fordeler i Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="28d59-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="28d59-106">Personlige kontakter kan være mottakere eller avhengige.</span><span class="sxs-lookup"><span data-stu-id="28d59-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="28d59-107">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Alternativer for rettighet for personlig kontakt**.</span><span class="sxs-lookup"><span data-stu-id="28d59-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="28d59-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="28d59-108">Select **New**.</span></span>

3. <span data-ttu-id="28d59-109">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="28d59-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="28d59-110">Felt</span><span class="sxs-lookup"><span data-stu-id="28d59-110">Field</span></span> | <span data-ttu-id="28d59-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="28d59-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="28d59-112">**Rettighetsalternativ**</span><span class="sxs-lookup"><span data-stu-id="28d59-112">**Eligibility option**</span></span> | <span data-ttu-id="28d59-113">Et unikt navn på et rettighetsalternativ eller en kode som identifiserer rettighetsalternativet.</span><span class="sxs-lookup"><span data-stu-id="28d59-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="28d59-114">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="28d59-114">**Description**</span></span> | <span data-ttu-id="28d59-115">En kort beskrivelse av rettighetsalternativet.</span><span class="sxs-lookup"><span data-stu-id="28d59-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="28d59-116">**Rettighetskode for kontakt**</span><span class="sxs-lookup"><span data-stu-id="28d59-116">**Contact eligibility code**</span></span> | <span data-ttu-id="28d59-117">Systemkoden som best beskriver det personlige rettighetsalternativet.</span><span class="sxs-lookup"><span data-stu-id="28d59-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="28d59-118">Du kan velge blant:</span><span class="sxs-lookup"><span data-stu-id="28d59-118">You can choose from:</span></span> <ul><li><span data-ttu-id="28d59-119">Relasjon</span><span class="sxs-lookup"><span data-stu-id="28d59-119">Relationship</span></span></li><li><span data-ttu-id="28d59-120">Student</span><span class="sxs-lookup"><span data-stu-id="28d59-120">Student</span></span></li><li><span data-ttu-id="28d59-121">Overårig avhengig</span><span class="sxs-lookup"><span data-stu-id="28d59-121">Overage dependent</span></span></li><li><span data-ttu-id="28d59-122">Overårig avhengig som er ufør</span><span class="sxs-lookup"><span data-stu-id="28d59-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="28d59-123">**Status**</span><span class="sxs-lookup"><span data-stu-id="28d59-123">**Status**</span></span> | <span data-ttu-id="28d59-124">Statusen for rettighetsalternativet.</span><span class="sxs-lookup"><span data-stu-id="28d59-124">The status of the eligibility option.</span></span> <span data-ttu-id="28d59-125">Hvis statusen for et rettighetsalternativ er satt til Inaktiv, kan du ikke velge dette rettighetsalternativet for personlige kontakter.</span><span class="sxs-lookup"><span data-stu-id="28d59-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="28d59-126">**Relasjon**</span><span class="sxs-lookup"><span data-stu-id="28d59-126">**Relationship**</span></span> | <span data-ttu-id="28d59-127">Angir relasjonen mellom den personlige kontakten og den ansatte.</span><span class="sxs-lookup"><span data-stu-id="28d59-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="28d59-128">Dette feltet er bare aktivt hvis kontaktrettighetskoden er satt til Relasjon.</span><span class="sxs-lookup"><span data-stu-id="28d59-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="28d59-129">**Alder**</span><span class="sxs-lookup"><span data-stu-id="28d59-129">**Age**</span></span> | <span data-ttu-id="28d59-130">Maksimal alder på en personlig kontakt for fordelsplanen.</span><span class="sxs-lookup"><span data-stu-id="28d59-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="28d59-131">Dette feltet er bare aktivt hvis du velger en relasjon.</span><span class="sxs-lookup"><span data-stu-id="28d59-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="28d59-132">Denne alderen sammenlignes med den beregnede alderen på den personlige kontakten.</span><span class="sxs-lookup"><span data-stu-id="28d59-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="28d59-133">Beregnet alder er: (dekningsdato – fødselsdato for personlig kontakt / 365).</span><span class="sxs-lookup"><span data-stu-id="28d59-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="28d59-134">Dette tallet er alltid et heltall.</span><span class="sxs-lookup"><span data-stu-id="28d59-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="28d59-135">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="28d59-135">Select **Save**.</span></span> 
