---
title: Konfigurere fradrag
description: ''
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010092"
---
# <a name="configure-deductions"></a><span data-ttu-id="5a6c5-102">Konfigurere fradrag</span><span class="sxs-lookup"><span data-stu-id="5a6c5-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5a6c5-103">Bruk fradrag i Microsoft Dynamics 365 Human Resources for å fastslå hvor mye hvis det er, hvis noe, å trekke fra en ansatts lønn for hver fordel.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="5a6c5-104">Fradrag gjelder for dato, slik at du kan holde en historisk oversikt over fradragsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="5a6c5-105">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Fradrag**.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="5a6c5-106">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-106">Select **New**.</span></span>

3. <span data-ttu-id="5a6c5-107">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="5a6c5-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5a6c5-108">Felt</span><span class="sxs-lookup"><span data-stu-id="5a6c5-108">Field</span></span> | <span data-ttu-id="5a6c5-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5a6c5-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5a6c5-110">Fradrag</span><span class="sxs-lookup"><span data-stu-id="5a6c5-110">Deduction</span></span> | <span data-ttu-id="5a6c5-111">En unik ID som brukes til å identifisere fordelsfradraget.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="5a6c5-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5a6c5-112">Description</span></span> | <span data-ttu-id="5a6c5-113">En beskrivelse for fradraget.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="5a6c5-114">Effektiv</span><span class="sxs-lookup"><span data-stu-id="5a6c5-114">Effective</span></span> | <span data-ttu-id="5a6c5-115">Startdatoen.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-115">The start date.</span></span> <span data-ttu-id="5a6c5-116">Standardverdien er gjeldende systemdato.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="5a6c5-117">Utløp</span><span class="sxs-lookup"><span data-stu-id="5a6c5-117">Expiration</span></span> | <span data-ttu-id="5a6c5-118">Sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-118">The end date.</span></span> <span data-ttu-id="5a6c5-119">Standardverdien er 12/31/2154, som i praksis betyr aldri.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="5a6c5-120">Overskrift</span><span class="sxs-lookup"><span data-stu-id="5a6c5-120">Heading</span></span> | <span data-ttu-id="5a6c5-121">Overskriftskoden fra lønnssystemet som dette fradraget vil bruke for den ansattes del av fradraget, ved behandling av fordelene til lønn.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="5a6c5-122">Dette brukes når du bruker en tredjeparts lønnsleverandør.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="5a6c5-123">Referanse for lønnstrekk for ansatt</span><span class="sxs-lookup"><span data-stu-id="5a6c5-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="5a6c5-124">Fradragskoden fra lønnssystemet som dette fradraget bruker for ansattdelen av fradraget ved behandling av fordelene til lønn.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="5a6c5-125">Beløpsoverskrift</span><span class="sxs-lookup"><span data-stu-id="5a6c5-125">Amount heading</span></span> | <span data-ttu-id="5a6c5-126">Overskriftskoden fra lønnssystemet som dette fradragsbeløpet vil bruke for den ansattes del av fradraget, ved behandling av fordelene til lønn.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="5a6c5-127">Dette brukes normalt når du bruker en tredjeparts lønnsleverandør.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="5a6c5-128">Kan slette</span><span class="sxs-lookup"><span data-stu-id="5a6c5-128">Can delete</span></span> | <span data-ttu-id="5a6c5-129">Angir om en eksportert verdi fra Dynamics 365 for Finance and Operations kan føre til at verdien slettes i lønningssystemet.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="5a6c5-130">Parede kolonner</span><span class="sxs-lookup"><span data-stu-id="5a6c5-130">Paired columns</span></span> | <span data-ttu-id="5a6c5-131">Angir om overskrift og fradragsbeløp skal eksporteres i parede sammenliggende kolonner til et lønningssystemet.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="5a6c5-132">Ikrafttredelsesdato for endring</span><span class="sxs-lookup"><span data-stu-id="5a6c5-132">Change effective date</span></span> | <span data-ttu-id="5a6c5-133">Datoen når endringen av fordelsfradraget settes i kraft.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="5a6c5-134">På denne datoen vil systemet automatisk endre fordelsfradraget og oppdatere alle fordelsplanene som er knyttet til dette fradraget, så lenge du kjører behandling av oppdatering av fradragsendring.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="5a6c5-135">Fradragsendring fullført</span><span class="sxs-lookup"><span data-stu-id="5a6c5-135">Deduction change completed</span></span> | <span data-ttu-id="5a6c5-136">Avmerkingsboksen for Fradragsendring fullført blir valgt automatisk når fordelsfradragsendringene er fullført av fradrag av oppdaterings endrings behandling.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="5a6c5-137">Hvis du vil spore og vedlikeholde endringer i fordelssatsoppsettet, velger du **Handlinger** og deretter **Vedlikehold versjoner**.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="5a6c5-138">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="5a6c5-138">Select **Save**.</span></span> 
