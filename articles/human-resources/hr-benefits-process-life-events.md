---
title: Behandle levetidshendelser
description: I løpet av den ansattes livssyklus i Microsoft Dynamics 365 Human Resources kan hver ansatt støte på forskjellige endringer av levetidshendelser.
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
ms.openlocfilehash: 91812432ead4b0afccfba30f8023f014e216236a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010082"
---
# <a name="process-life-events"></a><span data-ttu-id="9c72c-103">Behandle levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="9c72c-103">Process life events</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="9c72c-104">I løpet av den ansattes livssyklus i Microsoft Dynamics 365 Human Resources kan hver ansatt støte på forskjellige endringer av levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="9c72c-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="9c72c-105">For eksempel giftermål, endring i ansettelse eller endring av avhengig/mottaker.</span><span class="sxs-lookup"><span data-stu-id="9c72c-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="9c72c-106">Hvis du vil bruke levetidhendelser, må du aktivere levetidshendelser i skjemaet for fordelsparametere, definere livshendelsestyper og konfigurere livshendelsesalternativer for plantyper.</span><span class="sxs-lookup"><span data-stu-id="9c72c-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="9c72c-107">Før du kan behandle livshendelser, må du allerede kjøre åpen registrering minst én gang i løpet av en tidsramme for ansettelsen.</span><span class="sxs-lookup"><span data-stu-id="9c72c-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="9c72c-108">I USA blir det vanligvis åpen registrering én gang per år.</span><span class="sxs-lookup"><span data-stu-id="9c72c-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="9c72c-109">Utenfor USA kan åpen registrering kjøres på ansettelsestidspunktet.</span><span class="sxs-lookup"><span data-stu-id="9c72c-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="9c72c-110">En arbeider trenger ikke å velge en fordelsplan for at levetidshendelser skal behandles, men de må være inkludert i åpen registreringsbehandling.</span><span class="sxs-lookup"><span data-stu-id="9c72c-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="9c72c-111">Bruk behandling av levetidshendelser når du har arbeidere som har livshendelser som inntreffer på en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="9c72c-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="9c72c-112">Denne hendelsen behandler alle levetidshendelser som ikke er behandlet (for eksempel fremtidige levetidshendelser, eller levetidshendelser som ikke er spesifikke for én arbeider – ett eksempel er en ny fordel).</span><span class="sxs-lookup"><span data-stu-id="9c72c-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="9c72c-113">Livshendelser i sanntid skjules.</span><span class="sxs-lookup"><span data-stu-id="9c72c-113">Real time life events are hidden.</span></span>

<span data-ttu-id="9c72c-114">Hvis for eksempel i dag er 1. februar, og den 14. februar er arbeideren Jon Nilsen planlagt å endre juridiske enheter, hvis du kjører behandling av levetid for den 15. februar, behandler systemet alle hendelsene inntil 15. februar.</span><span class="sxs-lookup"><span data-stu-id="9c72c-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="9c72c-115">I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Behandling av levetidshendelse**.</span><span class="sxs-lookup"><span data-stu-id="9c72c-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="9c72c-116">I dialogboksen **Kjør prosess for levetidshendelse** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="9c72c-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="9c72c-117">Felt</span><span class="sxs-lookup"><span data-stu-id="9c72c-117">Field</span></span> | <span data-ttu-id="9c72c-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9c72c-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9c72c-119">Registreringsperiode</span><span class="sxs-lookup"><span data-stu-id="9c72c-119">Enrollment period</span></span> | <span data-ttu-id="9c72c-120">Registreringsperioden som det skal behandles levetidshendelser for.</span><span class="sxs-lookup"><span data-stu-id="9c72c-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="9c72c-121">Juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="9c72c-121">Legal entity</span></span> | <span data-ttu-id="9c72c-122">Den juridiske enheten som det skal behandles levetidshendelser for.</span><span class="sxs-lookup"><span data-stu-id="9c72c-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="9c72c-123">Levetidshendelsesdato</span><span class="sxs-lookup"><span data-stu-id="9c72c-123">Life event date</span></span> | <span data-ttu-id="9c72c-124">Systemet behandler alle hendelser i løpet av registreringsperioden som inntreffer frem til denne datoen.</span><span class="sxs-lookup"><span data-stu-id="9c72c-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="9c72c-125">Arbeider</span><span class="sxs-lookup"><span data-stu-id="9c72c-125">Worker</span></span> | <span data-ttu-id="9c72c-126">Arbeideren som det skal behandles levetidshendelser for.</span><span class="sxs-lookup"><span data-stu-id="9c72c-126">The worker to process life events for.</span></span> <span data-ttu-id="9c72c-127">Hvis du lar dette feltet stå tomt, blir livshendelser behandlet for alle arbeidere.</span><span class="sxs-lookup"><span data-stu-id="9c72c-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="9c72c-128">Hvis du vil kjøre prosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="9c72c-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="9c72c-129">Angi informasjon for prosessen.</span><span class="sxs-lookup"><span data-stu-id="9c72c-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="9c72c-130">Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c72c-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="9c72c-131">Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c72c-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="9c72c-132">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c72c-132">Select **OK**.</span></span> <span data-ttu-id="9c72c-133">Prosessen vil kjøre med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="9c72c-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="9c72c-134">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c72c-134">Select **OK**.</span></span>