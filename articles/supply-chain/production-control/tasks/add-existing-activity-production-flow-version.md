--- 
title: Legge til en eksisterende aktivitet i en produksjonsflytversjon
description: "Når du oppretter nye versjoner av produksjonsflyter, kan du velge å legge til aktiviteter som er opprettet for eldre versjoner, til den nye versjonen."
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 032855125ccd14fbdc1e1bdb735c92ce70853fb0
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="53075-103">Legge til en eksisterende aktivitet i en produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="53075-103">Add an existing activity to a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53075-104">Når du oppretter nye versjoner av produksjonsflyter, kan du velge å legge til aktiviteter som er opprettet for eldre versjoner, til den nye versjonen.</span><span class="sxs-lookup"><span data-stu-id="53075-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="53075-105">Denne fremgangsmåten viser hvordan en ny versjon opprettes for en eksisterende produksjonsflyt, uten å kopiere aktivitetene.</span><span class="sxs-lookup"><span data-stu-id="53075-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="53075-106">I det neste trinnet legges en eksisterende aktivitet til den nye versjonen.</span><span class="sxs-lookup"><span data-stu-id="53075-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="53075-107">Denne oppgaven krever produksjonsflyt med versjon og aktiviteter som allerede er opprettet.</span><span class="sxs-lookup"><span data-stu-id="53075-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="53075-108">Opprett en ny produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="53075-108">Create a new production flow version</span></span>
1. <span data-ttu-id="53075-109">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="53075-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="53075-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="53075-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="53075-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="53075-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="53075-112">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="53075-112">Click Edit.</span></span>
5. <span data-ttu-id="53075-113">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="53075-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="53075-114">Angi dato og klokkeslett i feltet Utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="53075-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="53075-115">Vær oppmerksom på at før du oppretter en ny produksjonsflytversjon, må du sjekke utløpsdatoen og -klokkeslettet for den aktive versjonen.</span><span class="sxs-lookup"><span data-stu-id="53075-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="53075-116">Den nye versjonen opprettes med en gyldig startdato som knyttes til utløpsdatoen for den valgte versjonen.</span><span class="sxs-lookup"><span data-stu-id="53075-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="53075-117">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="53075-117">Click Add.</span></span>
8. <span data-ttu-id="53075-118">Velg Nei i Kopier fra versjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="53075-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="53075-119">Velg Nei hvis du vil starte med en tom versjon hvis de fleste av aktivitetene i den kopierte versjonen vil bli erstattet av nye aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="53075-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="53075-120">Legg til de uendrede aktivitetene i Legg til eksisterende-funksjonen i aktivitetsskjemaet manuelt.</span><span class="sxs-lookup"><span data-stu-id="53075-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="53075-121">Velg Nei i feltet Dupliser Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="53075-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="53075-122">Når aktivitetene ikke kopieres til den nye versjonen, er det ikke mulig å kopiere Kanban-reglene på tidspunktet for opprettelsen av den nye versjonen.</span><span class="sxs-lookup"><span data-stu-id="53075-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="53075-123">I stedet bruker du funksjonen Opprett ny Kanban senere i Kanban-regel-skjemaet for å erstatte Kanban-regler for den gamle produksjonsflytversjonen med Kanban-regler som bruker aktivitetene i den nye versjonen.</span><span class="sxs-lookup"><span data-stu-id="53075-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="53075-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="53075-124">Click OK.</span></span>
11. <span data-ttu-id="53075-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="53075-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="53075-126">Legge til en eksisterende aktivitet</span><span class="sxs-lookup"><span data-stu-id="53075-126">Add an existing activity</span></span>
1. <span data-ttu-id="53075-127">Klikk Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="53075-127">Click Activities.</span></span>
2. <span data-ttu-id="53075-128">Klikk Legg til eksisterende for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="53075-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="53075-129">Finn og velg en eksisterende aktivitet som skal legges til den nye produksjonsflytversjonen.</span><span class="sxs-lookup"><span data-stu-id="53075-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="53075-130">Vær oppmerksom på at listen viser alle aktiviteter som er opprettet for denne produksjonsflyten for alle tidligere versjoner av flyten.</span><span class="sxs-lookup"><span data-stu-id="53075-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="53075-131">Angi eller velg en verdi i feltet Aktivitet.</span><span class="sxs-lookup"><span data-stu-id="53075-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="53075-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="53075-132">Click OK.</span></span>


