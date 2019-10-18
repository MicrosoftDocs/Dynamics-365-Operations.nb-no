---
title: Planlegg vedlikeholdsplaner
description: Dette emnet beskriver planlegging av vedlikeholdsplaner i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 698888533bf503838f455585f61cc7afc7239b05
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922051"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="f909f-103">Planlegg vedlikeholdsplaner</span><span class="sxs-lookup"><span data-stu-id="f909f-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f909f-104">Forebyggende vedlikeholdsplanlegging genererer kalenderoppføringer for aktiva, basert på oppsettet av vedlikeholdsplaner for aktivaene.</span><span class="sxs-lookup"><span data-stu-id="f909f-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="f909f-105">Du kan planlegge kalenderoppføringer basert på valgte vedlikeholdsplaner, anleggsmiddeltyper og anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="f909f-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="f909f-106">Klikk på **Aktivastyring** > **Periodisk** > **Forebyggende vedlikehold** > **Planlegg vedlikeholdsplaner**.</span><span class="sxs-lookup"><span data-stu-id="f909f-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="f909f-107">Du kan velge et tidsintervall i feltene **Periode** og **Periodefrekvens**.</span><span class="sxs-lookup"><span data-stu-id="f909f-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="f909f-108">Feltene **Periode** og **Periodefrekvens** angir hvor langt frem i tid du vil at vedlikeholdsplanlinjer skal opprettes, basert på vedlikeholdsplanene du har opprettet (tidsbasert eller tellerbasert).</span><span class="sxs-lookup"><span data-stu-id="f909f-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="f909f-109">I figuren nedenfor opprettes vedlikeholdsplanlinjer (= arbeidsordreforslag) fra gjeldende dato og tre måneder fremover.</span><span class="sxs-lookup"><span data-stu-id="f909f-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="f909f-110">Velg Ja på veksleknappen **Opprett automatisk hvis angitt i linjen** hvis arbeidsordrer skal opprettes automatisk i henhold til vedlikeholdsplanlinjen.</span><span class="sxs-lookup"><span data-stu-id="f909f-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="f909f-111">Hvis denne veksleknappen er satt til *Ja*, og det også er merket av for **Opprett automatisk** på vedlikeholdsplanlinjer i **Vedlikeholdsplaner**, opprettes arbeidsordrer på grunnlag av vedlikeholdsplanlinjene, og vedlikeholdsplanlinjer med statusen "Arbeidsordre opprettet" opprettes også.</span><span class="sxs-lookup"><span data-stu-id="f909f-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="f909f-112">Hvis bare ett alternativ er valgt (**Opprett automatisk hvis angitt i linjen**-veksleknappen i denne dialogboksen eller avmerkingsboksen **Opprett automatisk** i skjemaet **Vedlikeholdsplaner**), opprettes bare vedlikeholdsplanlinjer med statusen Opprettet.</span><span class="sxs-lookup"><span data-stu-id="f909f-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="f909f-113">I dette tilfellet opprettes ingen arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="f909f-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="f909f-114">Det er mulig å generere kalenderoppføringer basert på vedlikeholdsplaner (tid eller teller), aktiva, aktivatyper, arbeidssteder og arbeidsstedstyper.</span><span class="sxs-lookup"><span data-stu-id="f909f-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="f909f-115">Klikk på **Filter**-knappen, og gjør valg hvis nødvendig.</span><span class="sxs-lookup"><span data-stu-id="f909f-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="f909f-116">Når det gjelder planlegging av vedlikeholdsplaner på arbeidssteder: Hvis du oppdaterer oppsettet for aktivatyper, produsenter og modeller i vedlikeholdsplaner i **Alle arbeidssteder** > hurtigfanen **Vedlikeholdsplaner** etter at du har opprettet vedlikeholdsplaner, blir eksisterende oppføringer i vedlikeholdsplanen relatert til arbeidsstedet slettet automatisk.</span><span class="sxs-lookup"><span data-stu-id="f909f-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="f909f-117">Hvis du vil opprette nye kalenderoppføringer, som samsvarer med det oppdaterte vedlikeholdsplanoppsettet på arbeidsstedet, må du kjøre en ny tidsplan for vedlikeholdsplanen for dette arbeidsstedet.</span><span class="sxs-lookup"><span data-stu-id="f909f-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="f909f-118">Les mer om oppsettet av aktivatyper, produsenter og modeller på arbeidssteder i [Opprette arbeidssteder](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="f909f-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="f909f-119">*Eksempel:* Du vil opprette en vedlikeholdsplan for et bestemt arbeidssted, som betyr at alle anleggsmidler som er definert for dette arbeidsstedet på et gitt tidspunkt, blir tatt med når du planlegger vedlikeholdsplanen.</span><span class="sxs-lookup"><span data-stu-id="f909f-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="f909f-120">I dette tilfellet oppretter du en vedlikeholdsplan og velger det bestemte arbeidsstedet, men du legger IKKE til noen aktiva i vedlikeholdsplanen.</span><span class="sxs-lookup"><span data-stu-id="f909f-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any assets in the maintenance plan.</span></span> <span data-ttu-id="f909f-121">Resultatet er at når du planlegger denne vedlikeholdsplanen, opprettes vedlikeholdsplanlinjer for alle anleggsmidlene som er knyttet til arbeidsstedet på dette tidspunktet.</span><span class="sxs-lookup"><span data-stu-id="f909f-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="f909f-122">Hvis du endrer aktivatyper, produsenter og modeller i **Aktivatyper**, påvirker disse endringene bare nye anleggsmidler som bruker den oppdaterte aktivatypen.</span><span class="sxs-lookup"><span data-stu-id="f909f-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="f909f-123">Les mer om oppsett av anleggsmiddeltyper i [Aktivatyper](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="f909f-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="f909f-124">Klikk på **OK** for å starte genereringen av vedlikeholdsplanoppføringer for aktiva.</span><span class="sxs-lookup"><span data-stu-id="f909f-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="f909f-125">De genererte oppføringene vil vises på listesiden **Alle vedlikeholdsplaner**.</span><span class="sxs-lookup"><span data-stu-id="f909f-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span> <span data-ttu-id="f909f-126">Illustrasjonen nedenfor viser et eksempel på dialogboksen **Planlegg vedlikeholdsplaner**.</span><span class="sxs-lookup"><span data-stu-id="f909f-126">The following illustration shows an example of the **Schedule maintenance plans** dialog.</span></span>

![Figur 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="f909f-128">I dialogboksen **Planlegg vedlikeholdsplaner** kan du definere satsvise jobber i hurtigfanen **Kjør i bakgrunnen** for å generere kalenderoppføringer automatisk med jevne mellomrom.</span><span class="sxs-lookup"><span data-stu-id="f909f-128">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="f909f-129">Når du planlegger forebyggende vedlikehold, vil ikke vedlikeholdsplanlinjer med forventet startdato og -klokkeslett før systemdatoen og -klokkeslettet bli opprettet.</span><span class="sxs-lookup"><span data-stu-id="f909f-129">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="f909f-130">Figuren nedenfor gir en grafisk illustrasjon av en tidsbasert beregning av vedlikeholdsplan.</span><span class="sxs-lookup"><span data-stu-id="f909f-130">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![Figur 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="f909f-132">Angående tellerbaserte vedlikeholdsplaner: I figurene nedenfor vises to forskjellige tellerregistreringssykluser.</span><span class="sxs-lookup"><span data-stu-id="f909f-132">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="f909f-133">De er basert på en vedlikeholdsplan som er definert for anleggsmiddelet V0001, som forventer at aktivaet (en bil) kan kjøre cirka 2 000 km hver måned.</span><span class="sxs-lookup"><span data-stu-id="f909f-133">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="f909f-134">I det første eksemplet nås ikke de forventede 2 000 km hver måned.</span><span class="sxs-lookup"><span data-stu-id="f909f-134">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="f909f-135">I henhold til den tellerbaserte vedlikeholdsplanen, er terskelen 2 000 km. Dette betyr at når du kjører en planlegging av vedlikeholdsplan, skal det opprettes en vedlikeholdsplanlinje hver gang terskelen på 2 000 kilometer nås.</span><span class="sxs-lookup"><span data-stu-id="f909f-135">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="f909f-136">I eksempel 1 finnes det 4 registreringslinjer, men terskelen på 2 000 kilometer er bare nådd én gang.</span><span class="sxs-lookup"><span data-stu-id="f909f-136">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="f909f-137">Dette betyr at når du kjører planlegging av vedlikeholdsplaner for dette anleggsmidlet, for eksempel for en tre-måneders periode, vil det bare bli opprettet én vedlikeholdsplanlinje.</span><span class="sxs-lookup"><span data-stu-id="f909f-137">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="f909f-138">I den neste figuren er 2 000 km eller mer registrert hver måned.</span><span class="sxs-lookup"><span data-stu-id="f909f-138">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="f909f-139">Derfor opprettes det tre vedlikeholdslinjer hvis du planlegger vedlikeholdsplaner for dette anleggsmidlet for en periode på tre måneder.</span><span class="sxs-lookup"><span data-stu-id="f909f-139">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="f909f-140">Eksemplene som beskrives her, viser at alle tellerregistreringer som er utført for et anleggsmiddel, viser en trend som beskriver slitasje på aktivaet.</span><span class="sxs-lookup"><span data-stu-id="f909f-140">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="f909f-141">Trenden brukes som beregningsgrunnlag på tidspunktet for planleggingen av vedlikeholdsplanen.</span><span class="sxs-lookup"><span data-stu-id="f909f-141">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![Figur 3](media/11-preventive-maintenance.png)

![Figur 4](media/12-preventive-maintenance.png)

