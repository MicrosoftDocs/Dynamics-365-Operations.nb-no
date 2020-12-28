---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (10. september 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: ff5d21a8a71b068a276bedaf6e4b9964adcb4027
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462153"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a><span data-ttu-id="8b38c-103">Hva er nytt eller endret i Dynamics 365 Talent – Core HR (10. september 2018)</span><span class="sxs-lookup"><span data-stu-id="8b38c-103">What's new or changed in Dynamics 365 Talent - Core HR (September 10, 2018)</span></span>

<span data-ttu-id="8b38c-104">**Build 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="8b38c-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="8b38c-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="8b38c-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="8b38c-106">Tillat bestemt tidspunkt på dagen på forespørsler om fritid (halve dager)</span><span class="sxs-lookup"><span data-stu-id="8b38c-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="8b38c-107">Hvis permisjon og fravær er satt opp slik at fritid sendes inn i dager, kan du nå også muliggjøre en halvdagsdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="8b38c-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="8b38c-108">Når brukere deretter sender forespørsler om fritid, de kan angi om de vil ber om den første delen eller den andre delen av fridagen.</span><span class="sxs-lookup"><span data-stu-id="8b38c-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="8b38c-109">Dette alternativet deaktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="8b38c-109">By default, this option is turned off.</span></span> <span data-ttu-id="8b38c-110">For at ansatte skal kunne be om den første eller andre halvdelen av dagen, må du aktivere dette alternativet i området **Permisjon og fravær** i Personale-parameterne.</span><span class="sxs-lookup"><span data-stu-id="8b38c-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="8b38c-111">Sikkerhetsrettigheten for denne funksjonen er Oppretthold parametere for Personale.</span><span class="sxs-lookup"><span data-stu-id="8b38c-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="8b38c-112">Validering av permisjons og fraværsoppføringer</span><span class="sxs-lookup"><span data-stu-id="8b38c-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="8b38c-113">Avhengig av hvordan permisjon er konfigurert, vil ansatte som prøver å sende en forespørsel om fritid som er lengre enn deres virkedag, få en advarsel.</span><span class="sxs-lookup"><span data-stu-id="8b38c-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="8b38c-114">De blir med andre ord varslet hvis de prøver å ta mer enn en hel dag fri på en gitt dato.</span><span class="sxs-lookup"><span data-stu-id="8b38c-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="8b38c-115">Denne valideringen er alltid aktivert.</span><span class="sxs-lookup"><span data-stu-id="8b38c-115">This validation is always turned on.</span></span> <span data-ttu-id="8b38c-116">Hver gang ansatte overskrider dagsterskelen som er definert, får de en advarsel i fritidsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="8b38c-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="8b38c-117">Flere felt for betingelsesuttrykk i arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="8b38c-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="8b38c-118">Flere felt er lagt til for betingelsesuttrykk og plassholdere for flere arbeidsflyter i Core HR.</span><span class="sxs-lookup"><span data-stu-id="8b38c-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="8b38c-119">Følgende felt er lagt til i arbeidsflytene for kompensasjon, oppsigelse og overføring:</span><span class="sxs-lookup"><span data-stu-id="8b38c-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="8b38c-120">Ansettelsestype</span><span class="sxs-lookup"><span data-stu-id="8b38c-120">EmploymentType</span></span>
- <span data-ttu-id="8b38c-121">Juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="8b38c-121">LegalEntity</span></span>
- <span data-ttu-id="8b38c-122">Justert startdato for arbeider</span><span class="sxs-lookup"><span data-stu-id="8b38c-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="8b38c-123">Oppsigelsesvarsel for arbeidsgiver</span><span class="sxs-lookup"><span data-stu-id="8b38c-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="8b38c-124">Oppsigelsesenhet for arbeidsgiver</span><span class="sxs-lookup"><span data-stu-id="8b38c-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="8b38c-125">Overgangsdato</span><span class="sxs-lookup"><span data-stu-id="8b38c-125">TransitionDate</span></span>
- <span data-ttu-id="8b38c-126">Oppsigelsesvarsel for arbeider</span><span class="sxs-lookup"><span data-stu-id="8b38c-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="8b38c-127">Arbeiderens startdato</span><span class="sxs-lookup"><span data-stu-id="8b38c-127">WorkerStartDate</span></span>
- <span data-ttu-id="8b38c-128">Oppsigelsesenhet for arbeider</span><span class="sxs-lookup"><span data-stu-id="8b38c-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="8b38c-129">Sluttdato for prøvetid</span><span class="sxs-lookup"><span data-stu-id="8b38c-129">ProbationEndDate</span></span>
- <span data-ttu-id="8b38c-130">Posisjon</span><span class="sxs-lookup"><span data-stu-id="8b38c-130">Position</span></span>
- <span data-ttu-id="8b38c-131">Fagforening</span><span class="sxs-lookup"><span data-stu-id="8b38c-131">Union</span></span>
- <span data-ttu-id="8b38c-132">Avdeling</span><span class="sxs-lookup"><span data-stu-id="8b38c-132">Department</span></span>
- <span data-ttu-id="8b38c-133">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="8b38c-133">PositionType</span></span>
- <span data-ttu-id="8b38c-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="8b38c-134">CompLocation</span></span>
- <span data-ttu-id="8b38c-135">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="8b38c-135">Title</span></span>
- <span data-ttu-id="8b38c-136">Jobb</span><span class="sxs-lookup"><span data-stu-id="8b38c-136">Job</span></span>
- <span data-ttu-id="8b38c-137">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="8b38c-137">JobType</span></span>
- <span data-ttu-id="8b38c-138">Jobbserie</span><span class="sxs-lookup"><span data-stu-id="8b38c-138">JobFamily</span></span>
- <span data-ttu-id="8b38c-139">Jobbfunksjon</span><span class="sxs-lookup"><span data-stu-id="8b38c-139">JobFunction</span></span>

<span data-ttu-id="8b38c-140">Følgende felt er lagt til i arbeidsflyten for stilling:</span><span class="sxs-lookup"><span data-stu-id="8b38c-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="8b38c-141">Posisjon</span><span class="sxs-lookup"><span data-stu-id="8b38c-141">Position</span></span>
- <span data-ttu-id="8b38c-142">Fagforening</span><span class="sxs-lookup"><span data-stu-id="8b38c-142">Union</span></span>
- <span data-ttu-id="8b38c-143">Avdeling</span><span class="sxs-lookup"><span data-stu-id="8b38c-143">Department</span></span>
- <span data-ttu-id="8b38c-144">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="8b38c-144">PositionType</span></span>
- <span data-ttu-id="8b38c-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="8b38c-145">CompLocation</span></span>
- <span data-ttu-id="8b38c-146">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="8b38c-146">Title</span></span>
- <span data-ttu-id="8b38c-147">Jobb</span><span class="sxs-lookup"><span data-stu-id="8b38c-147">Job</span></span>
- <span data-ttu-id="8b38c-148">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="8b38c-148">JobType</span></span>
- <span data-ttu-id="8b38c-149">Jobbserie</span><span class="sxs-lookup"><span data-stu-id="8b38c-149">JobFamily</span></span>
- <span data-ttu-id="8b38c-150">Jobbfunksjon</span><span class="sxs-lookup"><span data-stu-id="8b38c-150">JobFunction</span></span>

<span data-ttu-id="8b38c-151">Feltene i betingelsesuttrykk og plassholdere er tilgjengelige for alle brukere som har tilgang til å konfigurere arbeidsflytene nevnt ovenfor.</span><span class="sxs-lookup"><span data-stu-id="8b38c-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="8b38c-152">Gå til Attract fra personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="8b38c-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="8b38c-153">I personaladministrasjon, hvis Attract ikke er satt opp i delen **Kandidater som skal ansettes**, blir brukerne dirigert til å komme i gang med Attract, i stedet for å vise meldingen "Fant ingenting å vise her".</span><span class="sxs-lookup"><span data-stu-id="8b38c-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="8b38c-154">Andre endringer</span><span class="sxs-lookup"><span data-stu-id="8b38c-154">Other changes</span></span>

<span data-ttu-id="8b38c-155">Denne versjonen inneholder flere andre feilrettinger:</span><span class="sxs-lookup"><span data-stu-id="8b38c-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="8b38c-156">Når en entreprenør ansettes, skal kategorien **Kompensasjon** ikke skal være tilgjengelig på forespørsels-/handlingssiden.</span><span class="sxs-lookup"><span data-stu-id="8b38c-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="8b38c-157">Under Be om avslutning-prosessen kan du ikke fortsette før alle nødvendige felt inneholder data.</span><span class="sxs-lookup"><span data-stu-id="8b38c-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="8b38c-158">Problemer med sorteringsrekkefølge og datovisning i analyse av personaladministrasjon er løst.</span><span class="sxs-lookup"><span data-stu-id="8b38c-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
