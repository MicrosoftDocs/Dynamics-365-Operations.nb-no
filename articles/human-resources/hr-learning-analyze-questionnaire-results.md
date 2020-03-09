---
title: Analysere resultat av spørreskjema
description: Spørreskjemastatistikk kan brukes til å beregne gjennomsnitt, totaler og prosenter basert på et sett med demografiske data.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d3b13ef7eda9943af35bbb37e3059dd81aa6365
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010116"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="8fb6f-103">Analysere resultat av spørreskjema</span><span class="sxs-lookup"><span data-stu-id="8fb6f-103">Analyzing questionnaire results</span></span>



<span data-ttu-id="8fb6f-104">Spørreskjemastatistikk kan brukes til å beregne gjennomsnitt, totaler og prosenter basert på et sett med demografiske data.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="8fb6f-105">Hvis du vil gjør dette, kan du gå til Spørreskjema > Vis og analyser resultater > Spørreskjemastatistikk.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="8fb6f-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="8fb6f-107">Opprette en post for spørreskjemastatistikk</span><span class="sxs-lookup"><span data-stu-id="8fb6f-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="8fb6f-108">Gå til Spørreskjemastatisitikk.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="8fb6f-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-109">Click New.</span></span>
3. <span data-ttu-id="8fb6f-110">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8fb6f-111">Skriv inn en verdi i Statistikk-feltet.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="8fb6f-112">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8fb6f-113">Klikk rullegardinknappen i Spørreskjema-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8fb6f-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8fb6f-115">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-115">Click the General tab.</span></span>
    * <span data-ttu-id="8fb6f-116">Velg om du vil ta med anonyme resultater eller resultater fra ansatte, kontaktpersoner og søkere.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="8fb6f-117">Merk av eller fjern merket i avmerkingsboksen Arbeider.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="8fb6f-118">Hvis du vil vise resultatene etter ansiennitet eller alder, angir du intervallene du vil bruke til å gruppere resultatene.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="8fb6f-119">Hvis du angir 5 for alderintervallet, grupperes resultatene etter fem års alderintervaller.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="8fb6f-120">Angi et tall i Alder-feltet.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="8fb6f-121">Velg om du vil kjøre beregningen mot hele spørreskjemaet, for hver resultatgruppe, for hvert spørsmål eller for hver spørsmålsrad.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="8fb6f-122">Velg hvordan du vil gruppere resultatene.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="8fb6f-123">Hvis du for eksempel beregner gjennomsnittlige poeng per spørsmål, vil du kanskje se spørsmålene gruppert etter resultatgruppe.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="8fb6f-124">Velg dataene som skal basere beregningen på.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="8fb6f-125">Hvis du for eksempel vil vise gjennomsnittlig prosent mottatt på spørreskjemaet på tvers av ansatte kontra gjennomsnittlig antall poeng som er oppnådd på tvers av ansatte.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="8fb6f-126">Klikk kategorien Område.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-126">Click the Range tab.</span></span>
    * <span data-ttu-id="8fb6f-127">Bruk områder til å begrense resultatsettet til bare de som oppfyller områdekriteriene.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="8fb6f-128">Klikk kategorien Gruppering av.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="8fb6f-129">Bruk Grupperinger til å bestemme hvordan resultatene skal vises.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="8fb6f-130">Du kan for eksempel gruppere resultatene først etter kjønn, deretter etter alder.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="8fb6f-131">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8fb6f-132">Flytt grupperingene til Valgt-siden og plasser dem i ønsket rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="8fb6f-133">Utføre statistikkberegningen</span><span class="sxs-lookup"><span data-stu-id="8fb6f-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="8fb6f-134">Klikk Utfør.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-134">Click Execute.</span></span>
    * <span data-ttu-id="8fb6f-135">Velg hvilken beregningsfunksjon du vil utføre på resultatene.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="8fb6f-136">Du kan for eksempel beregne gjennomsnittsprosentene på tvers av spørreskjemaet for de valgte grupperingene eller summere punktene på tvers av resultatgruppene for de valgte grupperingene.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="8fb6f-137">Merk av for eller fjern merkingen i avmerkingsboksen Slett tidligere søk.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="8fb6f-138">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="8fb6f-139">Vis resultatene av spørreskjemastatistikken.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="8fb6f-140">Klikk Resultat.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-140">Click Result.</span></span>
2. <span data-ttu-id="8fb6f-141">Klikk Resultat.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-141">Click Result.</span></span>
3. <span data-ttu-id="8fb6f-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-142">Close the page.</span></span>
