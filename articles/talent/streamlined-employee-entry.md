---
title: Strømlinjeformet ansattoppføring og navigasjon
description: Dataregistrering for arbeidere i Dynamics 365 Talent er forbedret for å tillate rask registrering for alle ansatte, tidligere, aktive eller fremtidige. En forenklet/konsolidert navigasjonsmodell er oppdatert for å finne relatert informasjon raskt og vise og foreta eventuelle nødvendige oppdateringer.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: 35cceb97442b05abc243cf7341e0ce7a0d09c613
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915207"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="29017-104">Strømlinjeformet ansattoppføring og navigasjon</span><span class="sxs-lookup"><span data-stu-id="29017-104">Streamlined employee entry and navigation</span></span>

<span data-ttu-id="29017-105">Dynamics 365 Talent muliggjør effektiv registrering av ansatte og ansettelsesdata.</span><span class="sxs-lookup"><span data-stu-id="29017-105">Dynamics 365 Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="29017-106">Du kan raskt oppdatere arbeidshistorikkinformasjon for tidligere, aktive og fremtidige ansatte og oppdragstakere.</span><span class="sxs-lookup"><span data-stu-id="29017-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="29017-107">Du kan også aktivere en forenklet navigasjonsopplevelse for å finne relatert informasjon raskt og foreta eventuelle nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="29017-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="29017-108">Denne funksjonaliteten er nå tilgjengelig i alle sandkassemiljøer.</span><span class="sxs-lookup"><span data-stu-id="29017-108">This functionality is now available in all environments.</span></span> <span data-ttu-id="29017-109">Hvis du vil aktivere denne funksjonen, går du til **System administrasjon > funksjonsbehandling > Ny > Strømlinjeformet ansattoppføring > Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="29017-109">To turn this feature on, navigate to **System administration > Feature Management > New > Streamlined employee entry > Enable**.</span></span> <span data-ttu-id="29017-110">Dette vil aktivere disse endringene for alle brukere.</span><span class="sxs-lookup"><span data-stu-id="29017-110">This will enable these changes for all users.</span></span> <span data-ttu-id="29017-111">Du kan når som helst deaktivere dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="29017-111">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="29017-112">Visningsalternativer</span><span class="sxs-lookup"><span data-stu-id="29017-112">View options</span></span>

<span data-ttu-id="29017-113">Du kan bruke **Visningsalternativer** i arbeiderskjemaet til å velge en kombinasjon av ansatte og oppdragstakere fra én liste.</span><span class="sxs-lookup"><span data-stu-id="29017-113">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="29017-114">Med disse alternativene kan du vise arbeidere på tvers av juridiske enheter eller for den juridiske enheten du er pålogget for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="29017-114">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="29017-115">Du kan også vise aktive, ventende og arbeidere som har sluttet, og du kan begrense resultater basert på typen arbeider (ansatt eller oppdragstaker).</span><span class="sxs-lookup"><span data-stu-id="29017-115">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="29017-116">Hvis avansert sikkerhet er aktivert, vil du bare se ansatte og oppdragstakere i de juridiske enhetene du har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="29017-116">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="29017-117">Kolonner i listevisningen endres basert på valgene dine.</span><span class="sxs-lookup"><span data-stu-id="29017-117">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="29017-118">Når du for eksempel viser ansatte som har sluttet, vises sluttdatoen og årsakskodene som tilleggskolonner i listen.</span><span class="sxs-lookup"><span data-stu-id="29017-118">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="29017-119">[![Visningsalternativer](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="29017-119">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="29017-120">Navigasjon og banner</span><span class="sxs-lookup"><span data-stu-id="29017-120">Navigation and banner</span></span>

<span data-ttu-id="29017-121">Et banner viser nøkkelinformasjon for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="29017-121">A banner displays key information for each worker.</span></span> <span data-ttu-id="29017-122">Banneret for aktive arbeidere viser følgende felt:</span><span class="sxs-lookup"><span data-stu-id="29017-122">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="29017-123">**Stillingstittel**</span><span class="sxs-lookup"><span data-stu-id="29017-123">**Title**</span></span>
- <span data-ttu-id="29017-124">**Avdeling**</span><span class="sxs-lookup"><span data-stu-id="29017-124">**Department**</span></span>
- <span data-ttu-id="29017-125">**Stillingstype**</span><span class="sxs-lookup"><span data-stu-id="29017-125">**Position type**</span></span>
- <span data-ttu-id="29017-126">**Arbeidertype**</span><span class="sxs-lookup"><span data-stu-id="29017-126">**Worker type**</span></span>
- <span data-ttu-id="29017-127">**Leder**</span><span class="sxs-lookup"><span data-stu-id="29017-127">**Manager**</span></span>
- <span data-ttu-id="29017-128">**Juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="29017-128">**Legal entity**</span></span>

<span data-ttu-id="29017-129">Banneret for arbeidere som har sluttet, viser følgende felt:</span><span class="sxs-lookup"><span data-stu-id="29017-129">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="29017-130">**Sluttdato**</span><span class="sxs-lookup"><span data-stu-id="29017-130">**Exited date**</span></span>
- <span data-ttu-id="29017-131">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="29017-131">**Reason**</span></span>

<span data-ttu-id="29017-132">Banneret for ventende ansatte viser følgende felt:</span><span class="sxs-lookup"><span data-stu-id="29017-132">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="29017-133">**Stillingstittel**</span><span class="sxs-lookup"><span data-stu-id="29017-133">**Title**</span></span>
- <span data-ttu-id="29017-134">**Avdeling**</span><span class="sxs-lookup"><span data-stu-id="29017-134">**Department**</span></span>
- <span data-ttu-id="29017-135">**Stillingstype**</span><span class="sxs-lookup"><span data-stu-id="29017-135">**Position type**</span></span>
- <span data-ttu-id="29017-136">**Leder**</span><span class="sxs-lookup"><span data-stu-id="29017-136">**Manager**</span></span>
- <span data-ttu-id="29017-137">**Startdato**</span><span class="sxs-lookup"><span data-stu-id="29017-137">**Starting date**</span></span>
- <span data-ttu-id="29017-138">**Juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="29017-138">**Legal entity**</span></span>

<span data-ttu-id="29017-139">Handlingsruten på siden for arbeideren er omorganisert for å inkludere færre alternativer.</span><span class="sxs-lookup"><span data-stu-id="29017-139">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="29017-140">Informasjonen er nå organisert i følgende kategorier:</span><span class="sxs-lookup"><span data-stu-id="29017-140">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="29017-141">Arbeid</span><span class="sxs-lookup"><span data-stu-id="29017-141">Work</span></span>
- <span data-ttu-id="29017-142">Person</span><span class="sxs-lookup"><span data-stu-id="29017-142">Person</span></span>
- <span data-ttu-id="29017-143">Permisjon</span><span class="sxs-lookup"><span data-stu-id="29017-143">Leave</span></span>
- <span data-ttu-id="29017-144">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="29017-144">Compensation</span></span>
- <span data-ttu-id="29017-145">Fordeler</span><span class="sxs-lookup"><span data-stu-id="29017-145">Benefits</span></span>
- <span data-ttu-id="29017-146">Samsvar</span><span class="sxs-lookup"><span data-stu-id="29017-146">Compliance</span></span>

<span data-ttu-id="29017-147">I tillegg gir den nye kategorien **Koblinger** på hovedsiden for arbeideren brukerne en sentral plassering der de kan få tilgang til all relatert informasjon for en arbeider.</span><span class="sxs-lookup"><span data-stu-id="29017-147">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="29017-148">På grunn av disse endringene kan informasjon vises på et annet sted enn du er vant til.</span><span class="sxs-lookup"><span data-stu-id="29017-148">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="29017-149">Lønnsinformasjon som tidligere ble vist i arbeiderskjemaet, vises for eksempel nå i handlingsruten under **Kompensasjon > Lønn**, og kategorien **Personlige opplysninger** har nå en **Mer informasjon**-knapp for å skjule felt som ikke brukes så ofte.</span><span class="sxs-lookup"><span data-stu-id="29017-149">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="29017-150">[![Banner](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="29017-150">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="29017-151">Arbeidshistorikk</span><span class="sxs-lookup"><span data-stu-id="29017-151">Work history</span></span>

<span data-ttu-id="29017-152">Kategorien **Arbeidshistorikk** viser arbeidshistorikken for alle juridiske enheter og er tilgjengelig for aktive og ventende ansatte og oppdragstakere samt de som har sluttet.</span><span class="sxs-lookup"><span data-stu-id="29017-152">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="29017-153">Du kan nå vise all arbeidshistorikk samtidig for de juridiske enhetene du har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="29017-153">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="29017-154">I tillegg kan du redigere informasjon for hver av arbeidshistorikkoppføringene uten å endre datakonteksten.</span><span class="sxs-lookup"><span data-stu-id="29017-154">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="29017-155">Du kan oppdatere all informasjon direkte på siden.</span><span class="sxs-lookup"><span data-stu-id="29017-155">You can update all information directly on the page.</span></span> 

<span data-ttu-id="29017-156">[![Arbeidshistorikk](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="29017-156">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="29017-157">Stillingshistorikk</span><span class="sxs-lookup"><span data-stu-id="29017-157">Position history</span></span>

<span data-ttu-id="29017-158">Kategorien **Stillinger** på hovedsiden for arbeidere gir en full oversikt over alle stillinger i organisasjonen, inkludert tidligere, nåværende og fremtidige utnevnelser.</span><span class="sxs-lookup"><span data-stu-id="29017-158">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="29017-159">Du kan fortsatt navigere direkte til arbeiderens stillingshistorikk i handlingsruten også.</span><span class="sxs-lookup"><span data-stu-id="29017-159">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="29017-160">[![Stillinger](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="29017-160">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

