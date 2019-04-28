---
title: Angi prosjekttimeregistreringer
description: Denne prosedyren lar deg opprette en timeregistrering ved hjelp av et tomt timeregistreringsskjema.
author: andreabichsel
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f1be02f0080ee23359ad905b1e997d8cd5adfd2
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "859143"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="0b5d0-103">Angi prosjekttimeregistreringer</span><span class="sxs-lookup"><span data-stu-id="0b5d0-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b5d0-104">Denne prosedyren lar deg opprette en timeregistrering ved hjelp av et tomt timeregistreringsskjema.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="0b5d0-105">Den nye timeregistreringen kan baseres på informasjon fra en tidligere timeregistrering, eller fra prosjekt- og aktivitetstilordninger på Mine favoritter-siden.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favorites page.</span></span> <span data-ttu-id="0b5d0-106">Som standard viser Alle timeregistreringer-listesiden alle timeregistreringene dine for den gjeldende perioden.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="0b5d0-107">Du kan bruke rullegardinlisten for Vis-feltet på Mine timeregistreringer-siden til å filtrere timeregistreringslisten etter tidsperiode eller prosjekt, eller til å vise timeregistreringer som ble opprettet på vegne av andre arbeidere.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="0b5d0-108">Demonstrasjonsdatafirmaet USSI brukes til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="0b5d0-109">Hvis du vil starte denne prosedyren, går du til Prosjektstyring og regnskap > Timeregistreringer > Mine timeregistreringer.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="0b5d0-110">Klikk Ny for å angi en ny timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="0b5d0-111">Rullegardinlisten Ressurs viser arbeideren som er tilordnet til den gjeldende brukeren, som standard.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="0b5d0-112">Hvis brukeren er angitt som representant, viser dette navnene slik at en bruker kan angi en timeregistrering på deres vegne.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="0b5d0-113">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="0b5d0-114">Hvis dette alternativet velges, opprettes nye timeregistreringslinjer ved hjelp av innstillingene for timeregistrering som ble konfigurert som favoritter.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
3. <span data-ttu-id="0b5d0-115">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-115">Click OK.</span></span>
4. <span data-ttu-id="0b5d0-116">Klikk Ny linje.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-116">Click New line.</span></span>
5. <span data-ttu-id="0b5d0-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0b5d0-118">Juridisk enhet-feltet viser som standard den gjeldende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="0b5d0-119">Klikk rullegardinknappen i Prosjekt-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0b5d0-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0b5d0-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0b5d0-122">Klikk rullegardinknappen i feltet Aktivitet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="0b5d0-123">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="0b5d0-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="0b5d0-125">Klikk rullegardinknappen i Kategori-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="0b5d0-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="0b5d0-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="0b5d0-128">Angi antall arbeidstimer for hver dag.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="0b5d0-129">Timer må angis i desimalformat.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="0b5d0-130">Hvis du arbeidet to timer og femten minutter, angir du 2,25.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="0b5d0-131">Angi antall arbeidstimer for hver dag.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="0b5d0-132">Timer må angis i desimalformat.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="0b5d0-133">Hvis du arbeidet to timer og femten minutter, angir du 2,25.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="0b5d0-134">Angi antall arbeidstimer for hver dag.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="0b5d0-135">Timer må angis i desimalformat.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="0b5d0-136">Hvis du arbeidet to timer og femten minutter, angir du 2,25.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="0b5d0-137">Angi antall arbeidstimer for hver dag.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="0b5d0-138">Timer må angis i desimalformat.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="0b5d0-139">Hvis du arbeidet to timer og femten minutter, angir du 2,25.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="0b5d0-140">Angi antall arbeidstimer for hver dag.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="0b5d0-141">Timer må angis i desimalformat.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="0b5d0-142">Hvis du arbeidet to timer og femten minutter, angir du 2,25.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="0b5d0-143">Følgende alternativer er tilgjengelige i Linjedetaljer:  o  Legge til informasjon om skatter og finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="0b5d0-144">o    Legge til kommentarer om timeregistreringslinjen.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="0b5d0-145">Klikk Arbeidsflyt for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="0b5d0-146">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-146">Click Submit.</span></span>
22. <span data-ttu-id="0b5d0-147">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-147">Click Submit.</span></span>

