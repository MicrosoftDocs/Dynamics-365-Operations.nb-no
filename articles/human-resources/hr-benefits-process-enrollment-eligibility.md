---
title: Fordelsregistreringsrettighet
description: Denne artikkelen beskriver hvordan du kjører prosessen for registreringsrettighet.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010017"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="2866a-103">Fordelsregistreringsrettighet</span><span class="sxs-lookup"><span data-stu-id="2866a-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2866a-104">Denne artikkelen beskriver hvordan du kjører prosessen for registreringsrettighet.</span><span class="sxs-lookup"><span data-stu-id="2866a-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="2866a-105">I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Behandling av registreringsrettighet**.</span><span class="sxs-lookup"><span data-stu-id="2866a-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="2866a-106">I dialogboksen **Kjør prosess for fordelsregistreringsrettighet** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="2866a-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="2866a-107">Felt</span><span class="sxs-lookup"><span data-stu-id="2866a-107">Field</span></span> | <span data-ttu-id="2866a-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2866a-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2866a-109">Registreringsperiode</span><span class="sxs-lookup"><span data-stu-id="2866a-109">Enrollment period</span></span> | <span data-ttu-id="2866a-110">Registreringsperioden som det skal behandles registreringsrettigheter for.</span><span class="sxs-lookup"><span data-stu-id="2866a-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="2866a-111">Juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="2866a-111">Legal entity</span></span> | <span data-ttu-id="2866a-112">Den juridiske enheten som det skal behandles registreringsrettigheter for.</span><span class="sxs-lookup"><span data-stu-id="2866a-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="2866a-113">Arbeider</span><span class="sxs-lookup"><span data-stu-id="2866a-113">Worker</span></span> | <span data-ttu-id="2866a-114">Arbeideren som det skal behandles registreringsrettigheter for.</span><span class="sxs-lookup"><span data-stu-id="2866a-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="2866a-115">Hvis du lar dette feltet stå tomt, blir registreringsrettigheten behandlet for alle arbeidere.</span><span class="sxs-lookup"><span data-stu-id="2866a-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="2866a-116">Fordelsplan</span><span class="sxs-lookup"><span data-stu-id="2866a-116">Benefit plan</span></span> | <span data-ttu-id="2866a-117">Fordelsplanen som det skal behandles registreringsrettigheter for.</span><span class="sxs-lookup"><span data-stu-id="2866a-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="2866a-118">Hvis du vil kjøre prosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="2866a-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="2866a-119">Angi informasjon for prosessen.</span><span class="sxs-lookup"><span data-stu-id="2866a-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="2866a-120">Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="2866a-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="2866a-121">Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2866a-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="2866a-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2866a-122">Select **OK**.</span></span> <span data-ttu-id="2866a-123">Prosessen vil kjøre med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="2866a-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="2866a-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2866a-124">Select **OK**.</span></span>
