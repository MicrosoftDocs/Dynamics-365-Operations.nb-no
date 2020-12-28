---
title: Angi prosjekttimeregistreringer
description: Denne prosedyren lar deg opprette en timeregistrering ved hjelp av et tomt timeregistreringsskjema.
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10dbb43cec47a758d11362947f27932a4911911a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419916"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="4eaa3-103">Angi prosjekttimeregistreringer</span><span class="sxs-lookup"><span data-stu-id="4eaa3-103">Enter project timesheets</span></span>



<span data-ttu-id="4eaa3-104">Denne prosedyren lar deg opprette en timeregistrering ved hjelp av et tomt timeregistreringsskjema.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="4eaa3-105">Den nye timeregistreringen kan baseres på informasjon fra en tidligere timeregistrering, eller fra prosjekt- og aktivitetstilordninger på **Mine favoritter**-siden.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="4eaa3-106">Som standard viser **Alle timeregistreringer**-listesiden alle timeregistreringene dine for den gjeldende perioden.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="4eaa3-107">Du kan bruke rullegardinlisten for **Vis**-feltet på **Mine timeregistreringer**-siden til å filtrere timeregistreringslisten etter tidsperiode eller prosjekt, eller til å vise timeregistreringer som ble opprettet på vegne av andre arbeidere.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="4eaa3-108">Demonstrasjonsdatafirmaet USSI brukes til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="4eaa3-109">I **navigasjonsruten** går du til **Moduler > Prosjektstyring og regnskap > Timeregistreringer > Mine timeregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="4eaa3-110">Klikk **Ny** for å angi en ny timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="4eaa3-111">Rullegardinlisten Ressurs viser arbeideren som er tilordnet til den gjeldende brukeren, som standard.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="4eaa3-112">Hvis brukeren er angitt som representant, viser dette navnene slik at en bruker kan angi en timeregistrering på deres vegne.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="4eaa3-113">Angi en dato i **Dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="4eaa3-114">Hvis dette alternativet velges, opprettes nye timeregistreringslinjer ved hjelp av innstillingene for timeregistrering som ble konfigurert som favoritter.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="4eaa3-115">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-115">Click **OK**.</span></span>
5. <span data-ttu-id="4eaa3-116">Klikk **Ny linje**.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-116">Click **New line**.</span></span>
6. <span data-ttu-id="4eaa3-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-117">In the list, mark the selected row.</span></span> <span data-ttu-id="4eaa3-118">**Juridisk enhet**-feltet viser som standard den gjeldende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="4eaa3-119">Klikk rullegardinknappen i **Prosjekt**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="4eaa3-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="4eaa3-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="4eaa3-122">Klikk rullegardinknappen i feltet **Aktivitetsnummer** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="4eaa3-123">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="4eaa3-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="4eaa3-125">Klikk rullegardinknappen i **Kategori**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="4eaa3-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="4eaa3-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="4eaa3-128">Angi antall arbeidstimer for hver dag.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="4eaa3-129">Angi timene i desimalformat.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="4eaa3-130">Hvis du arbeidet to timer og femten minutter, angir du 2,25.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="4eaa3-131">Følgende alternativer er tilgjengelige i **Linjedetaljer**:</span><span class="sxs-lookup"><span data-stu-id="4eaa3-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="4eaa3-132">Legg til informasjon om avgifter og finansdimensjoner i fanen **Generelt** og **Finansdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="4eaa3-133">Legg til kommentarer om timeregistreringslinjen i fanen **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="4eaa3-134">I **handlingsruten** klikker du **Arbeidsflyt** for å åpne dialogboksen for rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="4eaa3-135">Klikk **Send**.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-135">Click **Submit**.</span></span>
22. <span data-ttu-id="4eaa3-136">Klikk **Send**.</span><span class="sxs-lookup"><span data-stu-id="4eaa3-136">Click **Submit**.</span></span>

