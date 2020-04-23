---
title: Fordelsregistreringsrettighet
description: Denne artikkelen beskriver hvordan du kjører prosessen for registreringsrettighet.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1d978982213e713e362798c49aa57e6dc8b7a862
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230022"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="2b596-103">Fordelsregistreringsrettighet</span><span class="sxs-lookup"><span data-stu-id="2b596-103">Process enrollment eligibility</span></span>

<span data-ttu-id="2b596-104">Denne artikkelen beskriver hvordan du kjører prosessen for registreringsrettighet.</span><span class="sxs-lookup"><span data-stu-id="2b596-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="2b596-105">I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Behandling av registreringsrettighet**.</span><span class="sxs-lookup"><span data-stu-id="2b596-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="2b596-106">I dialogboksen **Kjør prosess for fordelsregistreringsrettighet** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="2b596-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="2b596-107">Felt</span><span class="sxs-lookup"><span data-stu-id="2b596-107">Field</span></span> | <span data-ttu-id="2b596-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2b596-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2b596-109">**Registreringsperiode**</span><span class="sxs-lookup"><span data-stu-id="2b596-109">**Enrollment period**</span></span> | <span data-ttu-id="2b596-110">Registreringsperioden som det skal behandles registreringsrettigheter for.</span><span class="sxs-lookup"><span data-stu-id="2b596-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="2b596-111">**Juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="2b596-111">**Legal entity**</span></span> | <span data-ttu-id="2b596-112">Den juridiske enheten som det skal behandles registreringsrettigheter for.</span><span class="sxs-lookup"><span data-stu-id="2b596-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="2b596-113">**Arbeider**</span><span class="sxs-lookup"><span data-stu-id="2b596-113">**Worker**</span></span> | <span data-ttu-id="2b596-114">Arbeideren som det skal behandles registreringsrettigheter for.</span><span class="sxs-lookup"><span data-stu-id="2b596-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="2b596-115">Hvis du lar dette feltet stå tomt, blir registreringsrettigheten behandlet for alle arbeidere.</span><span class="sxs-lookup"><span data-stu-id="2b596-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="2b596-116">**Fordelsplan**</span><span class="sxs-lookup"><span data-stu-id="2b596-116">**Benefit plan**</span></span> | <span data-ttu-id="2b596-117">Fordelsplanen som det skal behandles registreringsrettigheter for.</span><span class="sxs-lookup"><span data-stu-id="2b596-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="2b596-118">Hvis du vil kjøre prosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="2b596-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="2b596-119">Angi informasjon for prosessen.</span><span class="sxs-lookup"><span data-stu-id="2b596-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="2b596-120">Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b596-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="2b596-121">Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b596-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="2b596-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b596-122">Select **OK**.</span></span> <span data-ttu-id="2b596-123">Prosessen vil kjøre med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="2b596-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="2b596-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b596-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="2b596-125">Vis prosessresultater</span><span class="sxs-lookup"><span data-stu-id="2b596-125">View Process Results</span></span>

<span data-ttu-id="2b596-126">Denne artikkelen beskriver hvordan du viser resultater av en rettighetsprosess.</span><span class="sxs-lookup"><span data-stu-id="2b596-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="2b596-127">I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Prosessresultater**.</span><span class="sxs-lookup"><span data-stu-id="2b596-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="2b596-128">Følgende felt er angitt i skjemaet **Prosessresultater**:</span><span class="sxs-lookup"><span data-stu-id="2b596-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="2b596-129">Felt</span><span class="sxs-lookup"><span data-stu-id="2b596-129">Field</span></span> | <span data-ttu-id="2b596-130">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2b596-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2b596-131">**Prosess-ID**</span><span class="sxs-lookup"><span data-stu-id="2b596-131">**Process ID**</span></span> | <span data-ttu-id="2b596-132">Den unike ID-en for kombinasjonen av arbeider, juridisk enhet og prosesskjøring.</span><span class="sxs-lookup"><span data-stu-id="2b596-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="2b596-133">**Prosesstype**</span><span class="sxs-lookup"><span data-stu-id="2b596-133">**Process type**</span></span> | <span data-ttu-id="2b596-134">Dette identifiserer prosessen som ble kjørt.</span><span class="sxs-lookup"><span data-stu-id="2b596-134">This identifies the process that was run.</span></span> <span data-ttu-id="2b596-135">Eksempel: Registrering.</span><span class="sxs-lookup"><span data-stu-id="2b596-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="2b596-136">**Tidsangivelse**</span><span class="sxs-lookup"><span data-stu-id="2b596-136">**Time stamp**</span></span> | <span data-ttu-id="2b596-137">Tidspunktet da rettighetsprosessen ble kjørt.</span><span class="sxs-lookup"><span data-stu-id="2b596-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="2b596-138">**Juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="2b596-138">**Legal entity**</span></span> | <span data-ttu-id="2b596-139">Den juridiske enheten som ble angitt under registreringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="2b596-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="2b596-140">**Worker**</span><span class="sxs-lookup"><span data-stu-id="2b596-140">**Worker**</span></span> | <span data-ttu-id="2b596-141">Arbeideren som ble behandlet.</span><span class="sxs-lookup"><span data-stu-id="2b596-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="2b596-142">\*\*Plan</span><span class="sxs-lookup"><span data-stu-id="2b596-142">\*\*Plan</span></span> | <span data-ttu-id="2b596-143">Fordelsplanen som registreringen ble forsøkt utført for.</span><span class="sxs-lookup"><span data-stu-id="2b596-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="2b596-144">**Rettighetsregel**</span><span class="sxs-lookup"><span data-stu-id="2b596-144">**Eligibility rule**</span></span> | <span data-ttu-id="2b596-145">Rettighetsregelen som ble behandlet.</span><span class="sxs-lookup"><span data-stu-id="2b596-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="2b596-146">Hvis det oppstod en feil før rettigheten ble kjørt, vil dette være tomt.</span><span class="sxs-lookup"><span data-stu-id="2b596-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="2b596-147">Eksempel: Hvis kompensasjon ikke er definert for en arbeider, kan ikke rettighetsprosessen kjøres, og dette feltet blir stående tomt.</span><span class="sxs-lookup"><span data-stu-id="2b596-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="2b596-148">**Resultatstatus**</span><span class="sxs-lookup"><span data-stu-id="2b596-148">**Result status**</span></span> | <span data-ttu-id="2b596-149">Dette vil være Kvalifisert eller Ikke kvalifisert.</span><span class="sxs-lookup"><span data-stu-id="2b596-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="2b596-150">Resultatstatusen vil være Ikke kvalifisert hvis arbeideren ikke oppfyller rettighetsregelkriteriene, hvis arbeideren mangler nødvendig informasjon, for eksempel en betalingsfrekvens eller fast kompensasjon, eller hvis det mangler informasjon i fordelsplanen, og som forhindrer at arbeidere registreres.</span><span class="sxs-lookup"><span data-stu-id="2b596-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="2b596-151">**Resultatmelding**</span><span class="sxs-lookup"><span data-stu-id="2b596-151">**Result message**</span></span> | <span data-ttu-id="2b596-152">Indikerer hvorfor en arbeider ikke er kvalifisert for en fordelsplan, eller om rettighetsregelen ble bestått.</span><span class="sxs-lookup"><span data-stu-id="2b596-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

