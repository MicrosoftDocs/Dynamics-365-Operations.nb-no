---
title: Konfigurere fradrag
description: Bruk fradrag i Microsoft Dynamics 365 Human Resources for å fastslå hvor mye hvis det er, hvis noe, å trekke fra en ansatts lønn for hver fordel.
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
ms.openlocfilehash: 8cbe4de18334872e5a4c691864d703c95bd35559
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466164"
---
# <a name="configure-deductions"></a><span data-ttu-id="1aacc-103">Konfigurere fradrag</span><span class="sxs-lookup"><span data-stu-id="1aacc-103">Configure deductions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1aacc-104">Bruk fradrag i Microsoft Dynamics 365 Human Resources for å fastslå hvor mye hvis det er, hvis noe, å trekke fra en ansatts lønn for hver fordel.</span><span class="sxs-lookup"><span data-stu-id="1aacc-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="1aacc-105">Fradrag gjelder for dato, slik at du kan holde en historisk oversikt over fradragsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="1aacc-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="1aacc-106">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Fradrag**.</span><span class="sxs-lookup"><span data-stu-id="1aacc-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="1aacc-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1aacc-107">Select **New**.</span></span>

3. <span data-ttu-id="1aacc-108">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="1aacc-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1aacc-109">Felt</span><span class="sxs-lookup"><span data-stu-id="1aacc-109">Field</span></span> | <span data-ttu-id="1aacc-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1aacc-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1aacc-111">**Fradrag**</span><span class="sxs-lookup"><span data-stu-id="1aacc-111">**Deduction**</span></span> | <span data-ttu-id="1aacc-112">En unik ID som brukes til å identifisere fordelsfradraget.</span><span class="sxs-lookup"><span data-stu-id="1aacc-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="1aacc-113">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="1aacc-113">**Description**</span></span> | <span data-ttu-id="1aacc-114">En beskrivelse for fradraget.</span><span class="sxs-lookup"><span data-stu-id="1aacc-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="1aacc-115">**Effektiv**</span><span class="sxs-lookup"><span data-stu-id="1aacc-115">**Effective**</span></span> | <span data-ttu-id="1aacc-116">Startdatoen.</span><span class="sxs-lookup"><span data-stu-id="1aacc-116">The start date.</span></span> <span data-ttu-id="1aacc-117">Standardverdien er gjeldende systemdato.</span><span class="sxs-lookup"><span data-stu-id="1aacc-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="1aacc-118">**Utløp**</span><span class="sxs-lookup"><span data-stu-id="1aacc-118">**Expiration**</span></span> | <span data-ttu-id="1aacc-119">Sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="1aacc-119">The end date.</span></span> <span data-ttu-id="1aacc-120">Standardverdien er 12/31/2154, som i praksis betyr aldri.</span><span class="sxs-lookup"><span data-stu-id="1aacc-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="1aacc-121">**Overskrift**</span><span class="sxs-lookup"><span data-stu-id="1aacc-121">**Heading**</span></span> | <span data-ttu-id="1aacc-122">Overskriftskoden fra lønnssystemet som dette fradraget vil bruke for den ansattes del av fradraget, ved behandling av fordelene til lønn.</span><span class="sxs-lookup"><span data-stu-id="1aacc-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="1aacc-123">Dette brukes når du bruker en tredjeparts lønnsleverandør.</span><span class="sxs-lookup"><span data-stu-id="1aacc-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="1aacc-124">**Referanse for lønnstrekk for ansatt**</span><span class="sxs-lookup"><span data-stu-id="1aacc-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="1aacc-125">Fradragskoden fra lønnssystemet som dette fradraget bruker for ansattdelen av fradraget ved behandling av fordelene til lønn.</span><span class="sxs-lookup"><span data-stu-id="1aacc-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="1aacc-126">**Beløpsoverskrift**</span><span class="sxs-lookup"><span data-stu-id="1aacc-126">**Amount heading**</span></span> | <span data-ttu-id="1aacc-127">Overskriftskoden fra lønnssystemet som dette fradragsbeløpet vil bruke for den ansattes del av fradraget, ved behandling av fordelene til lønn.</span><span class="sxs-lookup"><span data-stu-id="1aacc-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="1aacc-128">Dette brukes normalt når du bruker en tredjeparts lønnsleverandør.</span><span class="sxs-lookup"><span data-stu-id="1aacc-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="1aacc-129">**Kan slette**</span><span class="sxs-lookup"><span data-stu-id="1aacc-129">**Can delete**</span></span> | <span data-ttu-id="1aacc-130">Angir om en eksportert verdi fra Dynamics 365 for Finance and Operations kan føre til at verdien slettes i lønningssystemet.</span><span class="sxs-lookup"><span data-stu-id="1aacc-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="1aacc-131">**Parede kolonner**</span><span class="sxs-lookup"><span data-stu-id="1aacc-131">**Paired columns**</span></span> | <span data-ttu-id="1aacc-132">Angir om overskrift og fradragsbeløp skal eksporteres i parede sammenliggende kolonner til et lønningssystemet.</span><span class="sxs-lookup"><span data-stu-id="1aacc-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="1aacc-133">**Ikrafttredelsesdato for endring**</span><span class="sxs-lookup"><span data-stu-id="1aacc-133">**Change effective date**</span></span> | <span data-ttu-id="1aacc-134">Datoen når endringen av fordelsfradraget settes i kraft.</span><span class="sxs-lookup"><span data-stu-id="1aacc-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="1aacc-135">På denne datoen endrer systemet automatisk fordelsfradraget og oppdaterer alle fordelsplanene som er knyttet til dette fradraget, så lenge du kjører behandling av **oppdatering av fradragsendring**.</span><span class="sxs-lookup"><span data-stu-id="1aacc-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="1aacc-136">**Fradragsendring fullført**</span><span class="sxs-lookup"><span data-stu-id="1aacc-136">**Deduction change completed**</span></span> | <span data-ttu-id="1aacc-137">Avmerkingsboksen for **Fradragsendring fullført** blir valgt automatisk når fordelsfradragsendringene er fullført av fradrag av oppdaterings endrings behandling.</span><span class="sxs-lookup"><span data-stu-id="1aacc-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="1aacc-138">Hvis du vil spore og vedlikeholde endringer i fordelssatsoppsettet, velger du **Handlinger** og deretter **Vedlikehold versjoner**.</span><span class="sxs-lookup"><span data-stu-id="1aacc-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="1aacc-139">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1aacc-139">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]