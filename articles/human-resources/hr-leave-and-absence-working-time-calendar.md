---
title: Opprette en driftstidskalender
description: Definer en driftstidskalender, helligdager og fritid i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 641f66c75875cfba51af3753223a070d7cb7dc50
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010109"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="7caef-103">Opprette en driftstidskalender</span><span class="sxs-lookup"><span data-stu-id="7caef-103">Create a working time calendar</span></span>

<span data-ttu-id="7caef-104">En driftstidskalender i Dynamics 365 Human Resources viser antall dager og timer som ansatte arbeider i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="7caef-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="7caef-105">Når en ansatt sender en avspaseringsforespørsel, trenger de ikke å bekymre seg for helligdager og lukking.</span><span class="sxs-lookup"><span data-stu-id="7caef-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="7caef-106">Hvis du vil effektivisere avspaseringsforespørsler, konfigurerer du disse elementene for organisasjonen:</span><span class="sxs-lookup"><span data-stu-id="7caef-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="7caef-107">Driftstidskalender</span><span class="sxs-lookup"><span data-stu-id="7caef-107">Working time calendar</span></span>
- <span data-ttu-id="7caef-108">Helligdager og lukkinger</span><span class="sxs-lookup"><span data-stu-id="7caef-108">Holidays and closures</span></span>
- <span data-ttu-id="7caef-109">Fritid</span><span class="sxs-lookup"><span data-stu-id="7caef-109">Non-work time</span></span>

<span data-ttu-id="7caef-110">Du kan legge til de to siste elementene mens du definerer en driftstidskalender.</span><span class="sxs-lookup"><span data-stu-id="7caef-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="7caef-111">Du kan også konfigurere eller oppdatere dem separat.</span><span class="sxs-lookup"><span data-stu-id="7caef-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="7caef-112">Definere en driftskalender</span><span class="sxs-lookup"><span data-stu-id="7caef-112">Set up a working time calendar</span></span>

<span data-ttu-id="7caef-113">Definer minst én driftstidskalender som viser driftsdager og driftstimer.</span><span class="sxs-lookup"><span data-stu-id="7caef-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="7caef-114">Hvis du har steder i flere land og områder, kan det være lurt å definere en driftstidskalender for hvert område.</span><span class="sxs-lookup"><span data-stu-id="7caef-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="7caef-115">På siden **Organisasjonsstyring** velger du **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="7caef-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="7caef-116">Velg **Ny**, og angi et navn og en beskrivelse for kalenderen.</span><span class="sxs-lookup"><span data-stu-id="7caef-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="7caef-117">Under **Genereringsalternativer** velger du arbeidsdagene for organisasjonen og angir arbeidstider.</span><span class="sxs-lookup"><span data-stu-id="7caef-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="7caef-118">Hvis du vil legge til en helligdag eller lukking, velger du **Legg til**-knappen ved siden av **Helligdager og lukkinger**.</span><span class="sxs-lookup"><span data-stu-id="7caef-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="7caef-119">Hvis du vil legge til fritid, som lunsjer eller pauser, velger du **Legg til** under **Fritid** og angir navnet og tidsperioden.</span><span class="sxs-lookup"><span data-stu-id="7caef-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="7caef-120">Under **Dager** velger du **Generer** for å generere dagene i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="7caef-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="7caef-121">Angi datoområdet for kalenderen, og velg deretter **Generer dager**.</span><span class="sxs-lookup"><span data-stu-id="7caef-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="7caef-122">Hvis du vil legge til arbeidsplaner, går du til **Arbeidsplan**, velger **Legg til** og angir deretter tidene for hver arbeidsplan.</span><span class="sxs-lookup"><span data-stu-id="7caef-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="7caef-123">Konfigurere helligdager og lukkinger</span><span class="sxs-lookup"><span data-stu-id="7caef-123">Configure holidays and closures</span></span>

<span data-ttu-id="7caef-124">Du kan legge til eller endre helligdager og lukkinger separat fra en driftstidskalender.</span><span class="sxs-lookup"><span data-stu-id="7caef-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="7caef-125">På siden **Organisasjonsstyring** velger du **Helligdager og lukkinger**.</span><span class="sxs-lookup"><span data-stu-id="7caef-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="7caef-126">Velg **Ny**, og angi et navn og en dato for helligdagen eller lukkingen.</span><span class="sxs-lookup"><span data-stu-id="7caef-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="7caef-127">Konfigurere fritid</span><span class="sxs-lookup"><span data-stu-id="7caef-127">Configure non-work time</span></span>

<span data-ttu-id="7caef-128">Du kan legge til eller endre tidspunkt for fritid separat fra en driftstidskalender.</span><span class="sxs-lookup"><span data-stu-id="7caef-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="7caef-129">På siden **Organisasjonsstyring** velger du **Fritid**.</span><span class="sxs-lookup"><span data-stu-id="7caef-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="7caef-130">Velg **Ny**, og angi et navn og et tidsomfang for fritiden.</span><span class="sxs-lookup"><span data-stu-id="7caef-130">Select **New** and enter a name and time range for the non-work time.</span></span>

## <a name="leave-and-absence-preview-feature"></a><span data-ttu-id="7caef-131">Forhåndsversjonsfunksjon for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="7caef-131">Leave and absence preview feature</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

<span data-ttu-id="7caef-132">Hvis du har aktivert forhåndsversjonsfunksjonen for korreksjon for helligdager for permisjon og fravær, bruker Human Resources helligdager og lukkingsdatoer til å bestemme hvor mange dager det skal justeres for ansatte som er registrert i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="7caef-132">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="7caef-133">Se også</span><span class="sxs-lookup"><span data-stu-id="7caef-133">See also</span></span>

- [<span data-ttu-id="7caef-134">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="7caef-134">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="7caef-135">Konfigurere permisjons- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="7caef-135">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
