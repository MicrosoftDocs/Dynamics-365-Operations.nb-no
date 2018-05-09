---
title: Opprette og behandle et avvik
description: "Bruk denne fremgangsmåten til å utføre behandling av avvik, basert på en eksisterende kvalitetsordre."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e73295698a17b7500db40820dd9603855810ca3a
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="65d6d-103">Opprette og behandle et avvik</span><span class="sxs-lookup"><span data-stu-id="65d6d-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65d6d-104">Bruk denne fremgangsmåten til å utføre behandling av avvik, basert på en eksisterende kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="65d6d-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="65d6d-105">Du kan kjøre denne registreringen i USMF demofirmaet, og du kan bruke de foreslåtte verdiene.</span><span class="sxs-lookup"><span data-stu-id="65d6d-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="65d6d-106">Denne prosedyren utføres vanligvis av en kvalitetsassistent.</span><span class="sxs-lookup"><span data-stu-id="65d6d-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="65d6d-107">Kjør oppgaveregistreringen "Kontrollere varekvaliteten" er en forutsetning.</span><span class="sxs-lookup"><span data-stu-id="65d6d-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="65d6d-108">Hvis du vil behandle godkjenningen av et avvik, må brukeren som kjører oppgaveregistreringen ha en "Navn"-verdi som er tilordnet på siden Brukere.</span><span class="sxs-lookup"><span data-stu-id="65d6d-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="65d6d-109">Hvis du vil bruke merknader i dokumentet, må brukeren også ha Dokumenthåndtering aktivert i brukeralternativene.</span><span class="sxs-lookup"><span data-stu-id="65d6d-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="65d6d-110">Velge en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="65d6d-110">Select a quality order</span></span>
1. <span data-ttu-id="65d6d-111">Gå til Kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="65d6d-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="65d6d-112">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="65d6d-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="65d6d-113">Velg kvalitetsordren som ble opprettet fra oppgaveregistrering Kontrollere varekvaliteten.</span><span class="sxs-lookup"><span data-stu-id="65d6d-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="65d6d-114">Opprette et avvik</span><span class="sxs-lookup"><span data-stu-id="65d6d-114">Create a nonconformance</span></span>
1. <span data-ttu-id="65d6d-115">Klikk Forespørsler.</span><span class="sxs-lookup"><span data-stu-id="65d6d-115">Click Inquiries.</span></span>
2. <span data-ttu-id="65d6d-116">Klikk Avvik.</span><span class="sxs-lookup"><span data-stu-id="65d6d-116">Click Non conformances.</span></span>
3. <span data-ttu-id="65d6d-117">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="65d6d-117">Click New.</span></span>
4. <span data-ttu-id="65d6d-118">Klikk rullegardinknappen i feltet Problemtype for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="65d6d-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="65d6d-119">Velg problemet som ble funnet under inspeksjonsprosessen.</span><span class="sxs-lookup"><span data-stu-id="65d6d-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="65d6d-120">Klikk rullegardinknappen i feltet Problemtype for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="65d6d-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="65d6d-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="65d6d-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="65d6d-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="65d6d-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="65d6d-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="65d6d-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="65d6d-124">Godkjenne/avvise et avvik</span><span class="sxs-lookup"><span data-stu-id="65d6d-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="65d6d-125">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="65d6d-125">Click Functions.</span></span>
2. <span data-ttu-id="65d6d-126">Klikk Godkjenn avvik.</span><span class="sxs-lookup"><span data-stu-id="65d6d-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="65d6d-127">Godkjenn avviket for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="65d6d-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="65d6d-128">Godkjente avvik kan knyttes til relaterte operasjoner for å registrere arbeid som utføres som en del av avvikshåndtering og, som i denne oppgaveregistreringen, behandling av rettelseshandlingen.</span><span class="sxs-lookup"><span data-stu-id="65d6d-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="65d6d-129">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="65d6d-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="65d6d-130">Opprette en rettelseshandling</span><span class="sxs-lookup"><span data-stu-id="65d6d-130">Create a correction action</span></span>
1. <span data-ttu-id="65d6d-131">Klikk Rettelser.</span><span class="sxs-lookup"><span data-stu-id="65d6d-131">Click Corrections.</span></span>
2. <span data-ttu-id="65d6d-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="65d6d-132">Click New.</span></span>
3. <span data-ttu-id="65d6d-133">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="65d6d-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="65d6d-134">Klikk rullegardinknappen i feltet Personalnummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="65d6d-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="65d6d-135">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="65d6d-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="65d6d-136">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="65d6d-136">Click Select.</span></span>
7. <span data-ttu-id="65d6d-137">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="65d6d-137">Click Attach.</span></span>
    * <span data-ttu-id="65d6d-138">Opprett en merknad om rettelsen.</span><span class="sxs-lookup"><span data-stu-id="65d6d-138">Create a note about the correction.</span></span> <span data-ttu-id="65d6d-139">I dette eksemplet er handlingen å kontakte leverandøren for å diskutere avvikssaken.</span><span class="sxs-lookup"><span data-stu-id="65d6d-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="65d6d-140">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="65d6d-140">Click New.</span></span>
9. <span data-ttu-id="65d6d-141">Klikk Notat.</span><span class="sxs-lookup"><span data-stu-id="65d6d-141">Click Note.</span></span>
    * <span data-ttu-id="65d6d-142">Legg merke til at, avhengig av oppsettet for rapporten, kan ulike dokumenttyper skrives ut på rapporter som er knyttet til behandling av avvik.</span><span class="sxs-lookup"><span data-stu-id="65d6d-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="65d6d-143">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="65d6d-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="65d6d-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="65d6d-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="65d6d-145">Vedlikeholde en korreksjon</span><span class="sxs-lookup"><span data-stu-id="65d6d-145">Maintain a correction</span></span>
1. <span data-ttu-id="65d6d-146">Klikk Merk som fullført.</span><span class="sxs-lookup"><span data-stu-id="65d6d-146">Click Mark complete.</span></span>
2. <span data-ttu-id="65d6d-147">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="65d6d-147">Click OK.</span></span>
3. <span data-ttu-id="65d6d-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="65d6d-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="65d6d-149">Lukke et avvik</span><span class="sxs-lookup"><span data-stu-id="65d6d-149">Close a nonconformance</span></span>
1. <span data-ttu-id="65d6d-150">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="65d6d-150">Click Functions.</span></span>
2. <span data-ttu-id="65d6d-151">Klikk Lukk avvik.</span><span class="sxs-lookup"><span data-stu-id="65d6d-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="65d6d-152">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="65d6d-152">Click Yes.</span></span>
4. <span data-ttu-id="65d6d-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="65d6d-153">Close the page.</span></span>
5. <span data-ttu-id="65d6d-154">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="65d6d-154">Close the page.</span></span>

