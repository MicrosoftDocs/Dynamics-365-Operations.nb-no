---
title: Angi prosjekttimeregistreringer
description: Denne prosedyren lar deg opprette en timeregistrering ved hjelp av et tomt timeregistreringsskjema.
author: andreabichsel
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd0389584cb723b403dcd5f6bec67d2eb969048f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565010"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="0b34b-103">Angi prosjekttimeregistreringer</span><span class="sxs-lookup"><span data-stu-id="0b34b-103">Enter project timesheets</span></span>

<span data-ttu-id="0b34b-104">Denne prosedyren lar deg opprette en timeregistrering ved hjelp av et tomt timeregistreringsskjema.</span><span class="sxs-lookup"><span data-stu-id="0b34b-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="0b34b-105">Den nye timeregistreringen kan baseres på informasjon fra en tidligere timeregistrering, eller fra prosjekt- og aktivitetstilordninger på **Mine favoritter**-siden.</span><span class="sxs-lookup"><span data-stu-id="0b34b-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="0b34b-106">Som standard viser **Alle timeregistreringer**-listesiden alle timeregistreringene dine for den gjeldende perioden.</span><span class="sxs-lookup"><span data-stu-id="0b34b-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="0b34b-107">Du kan bruke rullegardinlisten for **Vis**-feltet på **Mine timeregistreringer**-siden til å filtrere timeregistreringslisten etter tidsperiode eller prosjekt, eller til å vise timeregistreringer som ble opprettet på vegne av andre arbeidere.</span><span class="sxs-lookup"><span data-stu-id="0b34b-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="0b34b-108">Demonstrasjonsdatafirmaet USSI brukes til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="0b34b-108">The demo data company used to create this procedure is USSI.</span></span>  

1. <span data-ttu-id="0b34b-109">I **navigasjonsruten** går du til **Moduler > Prosjektstyring og regnskap > Timeregistreringer > Mine timeregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="0b34b-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="0b34b-110">Klikk på **Ny** for å angi en ny timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="0b34b-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="0b34b-111">Rullegardinlisten Ressurs viser arbeideren som er tilordnet til den gjeldende brukeren, som standard.</span><span class="sxs-lookup"><span data-stu-id="0b34b-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="0b34b-112">Hvis brukeren er angitt som representant, viser dette navnene slik at en bruker kan angi en timeregistrering på deres vegne.</span><span class="sxs-lookup"><span data-stu-id="0b34b-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="0b34b-113">Angi en dato i **Dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0b34b-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="0b34b-114">Hvis dette alternativet velges, opprettes nye timeregistreringslinjer ved hjelp av innstillingene for timeregistrering som ble konfigurert som favoritter.</span><span class="sxs-lookup"><span data-stu-id="0b34b-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="0b34b-115">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b34b-115">Click **OK**.</span></span>
5. <span data-ttu-id="0b34b-116">Klikk på **Ny linje**.</span><span class="sxs-lookup"><span data-stu-id="0b34b-116">Click **New line**.</span></span>
6. <span data-ttu-id="0b34b-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0b34b-117">In the list, mark the selected row.</span></span> <span data-ttu-id="0b34b-118">**Juridisk enhet**-feltet viser som standard den gjeldende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="0b34b-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="0b34b-119">Klikk på rullegardinknappen i **Prosjekt**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0b34b-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0b34b-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0b34b-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="0b34b-121">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0b34b-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="0b34b-122">Klikk på rullegardinknappen i feltet **Aktivitetsnummer** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0b34b-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0b34b-123">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0b34b-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="0b34b-124">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0b34b-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="0b34b-125">Klikk på rullegardinknappen i **Kategori**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0b34b-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="0b34b-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0b34b-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="0b34b-127">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0b34b-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="0b34b-128">Angi antall arbeidstimer for hver dag.</span><span class="sxs-lookup"><span data-stu-id="0b34b-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="0b34b-129">Angi timene i desimalformat.</span><span class="sxs-lookup"><span data-stu-id="0b34b-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="0b34b-130">Hvis du arbeidet to timer og femten minutter, angir du 2,25.</span><span class="sxs-lookup"><span data-stu-id="0b34b-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="0b34b-131">Følgende alternativer er tilgjengelige i **Linjedetaljer**:</span><span class="sxs-lookup"><span data-stu-id="0b34b-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="0b34b-132">Legg til informasjon om avgifter og finansdimensjoner i fanen **Generelt** og **Finansdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="0b34b-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="0b34b-133">Legg til kommentarer om timeregistreringslinjen i fanen **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="0b34b-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="0b34b-134">I **handlingsruten** klikker du **Arbeidsflyt** for å åpne dialogboksen for rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="0b34b-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="0b34b-135">Klikk på **Send**.</span><span class="sxs-lookup"><span data-stu-id="0b34b-135">Click **Submit**.</span></span>
22. <span data-ttu-id="0b34b-136">Klikk på **Send**.</span><span class="sxs-lookup"><span data-stu-id="0b34b-136">Click **Submit**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]