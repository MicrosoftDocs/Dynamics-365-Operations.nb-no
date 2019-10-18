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
ms.openlocfilehash: 40bbb8429355fa18fe12c7cf56f8d58f19766cad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009428"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="fc7bc-104">Strømlinjeformet ansattoppføring og navigasjon</span><span class="sxs-lookup"><span data-stu-id="fc7bc-104">Streamlined employee entry and navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc7bc-105">Dynamics 365 Talent muliggjør effektiv registrering av ansatte og ansettelsesdata.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-105">Dynamics 365 Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="fc7bc-106">Du kan raskt oppdatere arbeidshistorikkinformasjon for tidligere, aktive og fremtidige ansatte og oppdragstakere.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="fc7bc-107">Du kan også aktivere en forenklet navigasjonsopplevelse for å finne relatert informasjon raskt og foreta eventuelle nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="fc7bc-108">Denne funksjonaliteten er nå tilgjengelig i sandkassemiljøer.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-108">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="fc7bc-109">Hvis du vil aktivere denne funksjonen, går du til **Systemadministrasjon > Koblinger > Oppsett > Systemparametere> Forhåndsvisningsfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-109">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="fc7bc-110">Velg **Utvidet arbeiderskjema og navigering**.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-110">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="fc7bc-111">Dette vil aktivere disse endringene for alle brukere.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-111">This will enable these changes for all users.</span></span> <span data-ttu-id="fc7bc-112">Du kan når som helst deaktivere dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-112">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="fc7bc-113">Visningsalternativer</span><span class="sxs-lookup"><span data-stu-id="fc7bc-113">View options</span></span>

<span data-ttu-id="fc7bc-114">Du kan bruke **Visningsalternativer** i arbeiderskjemaet til å velge en kombinasjon av ansatte og oppdragstakere fra én liste.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-114">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="fc7bc-115">Med disse alternativene kan du vise arbeidere på tvers av juridiske enheter eller for den juridiske enheten du er pålogget for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-115">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="fc7bc-116">Du kan også vise aktive, ventende og arbeidere som har sluttet, og du kan begrense resultater basert på typen arbeider (ansatt eller oppdragstaker).</span><span class="sxs-lookup"><span data-stu-id="fc7bc-116">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="fc7bc-117">Hvis avansert sikkerhet er aktivert, vil du bare se ansatte og oppdragstakere i de juridiske enhetene du har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-117">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="fc7bc-118">Kolonner i listevisningen endres basert på valgene dine.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-118">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="fc7bc-119">Når du for eksempel viser ansatte som har sluttet, vises sluttdatoen og årsakskodene som tilleggskolonner i listen.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-119">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="fc7bc-120">[![Visningsalternativer](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="fc7bc-120">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="fc7bc-121">Navigasjon og banner</span><span class="sxs-lookup"><span data-stu-id="fc7bc-121">Navigation and banner</span></span>

<span data-ttu-id="fc7bc-122">Et banner viser nøkkelinformasjon for hver arbeider.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-122">A banner displays key information for each worker.</span></span> <span data-ttu-id="fc7bc-123">Banneret for aktive arbeidere viser følgende felt:</span><span class="sxs-lookup"><span data-stu-id="fc7bc-123">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="fc7bc-124">**Stillingstittel**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-124">**Title**</span></span>
- <span data-ttu-id="fc7bc-125">**Avdeling**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-125">**Department**</span></span>
- <span data-ttu-id="fc7bc-126">**Stillingstype**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-126">**Position type**</span></span>
- <span data-ttu-id="fc7bc-127">**Arbeidertype**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-127">**Worker type**</span></span>
- <span data-ttu-id="fc7bc-128">**Leder**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-128">**Manager**</span></span>
- <span data-ttu-id="fc7bc-129">**Juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-129">**Legal entity**</span></span>

<span data-ttu-id="fc7bc-130">Banneret for arbeidere som har sluttet, viser følgende felt:</span><span class="sxs-lookup"><span data-stu-id="fc7bc-130">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="fc7bc-131">**Sluttdato**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-131">**Exited date**</span></span>
- <span data-ttu-id="fc7bc-132">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-132">**Reason**</span></span>

<span data-ttu-id="fc7bc-133">Banneret for ventende ansatte viser følgende felt:</span><span class="sxs-lookup"><span data-stu-id="fc7bc-133">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="fc7bc-134">**Stillingstittel**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-134">**Title**</span></span>
- <span data-ttu-id="fc7bc-135">**Avdeling**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-135">**Department**</span></span>
- <span data-ttu-id="fc7bc-136">**Stillingstype**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-136">**Position type**</span></span>
- <span data-ttu-id="fc7bc-137">**Leder**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-137">**Manager**</span></span>
- <span data-ttu-id="fc7bc-138">**Startdato**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-138">**Starting date**</span></span>
- <span data-ttu-id="fc7bc-139">**Juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="fc7bc-139">**Legal entity**</span></span>

<span data-ttu-id="fc7bc-140">Handlingsruten på siden for arbeideren er omorganisert for å inkludere færre alternativer.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-140">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="fc7bc-141">Informasjonen er nå organisert i følgende kategorier:</span><span class="sxs-lookup"><span data-stu-id="fc7bc-141">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="fc7bc-142">Arbeid</span><span class="sxs-lookup"><span data-stu-id="fc7bc-142">Work</span></span>
- <span data-ttu-id="fc7bc-143">Person</span><span class="sxs-lookup"><span data-stu-id="fc7bc-143">Person</span></span>
- <span data-ttu-id="fc7bc-144">Permisjon</span><span class="sxs-lookup"><span data-stu-id="fc7bc-144">Leave</span></span>
- <span data-ttu-id="fc7bc-145">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="fc7bc-145">Compensation</span></span>
- <span data-ttu-id="fc7bc-146">Fordeler</span><span class="sxs-lookup"><span data-stu-id="fc7bc-146">Benefits</span></span>
- <span data-ttu-id="fc7bc-147">Samsvar</span><span class="sxs-lookup"><span data-stu-id="fc7bc-147">Compliance</span></span>

<span data-ttu-id="fc7bc-148">I tillegg gir den nye kategorien **Koblinger** på hovedsiden for arbeideren brukerne en sentral plassering der de kan få tilgang til all relatert informasjon for en arbeider.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-148">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="fc7bc-149">På grunn av disse endringene kan informasjon vises på et annet sted enn du er vant til.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-149">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="fc7bc-150">Lønnsinformasjon som tidligere ble vist i arbeiderskjemaet, vises for eksempel nå i handlingsruten under **Kompensasjon > Lønn**, og kategorien **Personlige opplysninger** har nå en **Mer informasjon**-knapp for å skjule felt som ikke brukes så ofte.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-150">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="fc7bc-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="fc7bc-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="fc7bc-152">Arbeidshistorikk</span><span class="sxs-lookup"><span data-stu-id="fc7bc-152">Work history</span></span>

<span data-ttu-id="fc7bc-153">Kategorien **Arbeidshistorikk** viser arbeidshistorikken for alle juridiske enheter og er tilgjengelig for aktive og ventende ansatte og oppdragstakere samt de som har sluttet.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-153">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="fc7bc-154">Du kan nå vise all arbeidshistorikk samtidig for de juridiske enhetene du har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-154">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="fc7bc-155">I tillegg kan du redigere informasjon for hver av arbeidshistorikkoppføringene uten å endre datakonteksten.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-155">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="fc7bc-156">Du kan oppdatere all informasjon direkte på siden.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-156">You can update all information directly on the page.</span></span> 

<span data-ttu-id="fc7bc-157">[![Arbeidshistorikk](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="fc7bc-157">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="fc7bc-158">Stillingshistorikk</span><span class="sxs-lookup"><span data-stu-id="fc7bc-158">Position history</span></span>

<span data-ttu-id="fc7bc-159">Kategorien **Stillinger** på hovedsiden for arbeidere gir en full oversikt over alle stillinger i organisasjonen, inkludert tidligere, nåværende og fremtidige utnevnelser.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-159">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="fc7bc-160">Du kan fortsatt navigere direkte til arbeiderens stillingshistorikk i handlingsruten også.</span><span class="sxs-lookup"><span data-stu-id="fc7bc-160">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="fc7bc-161">[![Stillinger](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="fc7bc-161">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

