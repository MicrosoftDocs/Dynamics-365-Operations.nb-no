---
title: Opprette og behandle et avvik
description: Dette emnet forklarer hvordan du utfører behandling av avvik, basert på en eksisterende kvalitetsordre.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4525e79cb388cc9bbcfe1d038a53cf53916a678c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008100"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="a6510-103">Opprette og behandle et avvik</span><span class="sxs-lookup"><span data-stu-id="a6510-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6510-104">Dette emnet forklarer hvordan du utfører behandling av avvik, basert på en eksisterende kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="a6510-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="a6510-105">Du kan kjøre denne registreringen i USMF demofirmaet, og du kan bruke de foreslåtte verdiene.</span><span class="sxs-lookup"><span data-stu-id="a6510-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="a6510-106">Denne prosedyren utføres vanligvis av en kvalitetsassistent.</span><span class="sxs-lookup"><span data-stu-id="a6510-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="a6510-107">Fullføring av instruksjonene i [Kontrollere varekvaliteten](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) er en forutsetning.</span><span class="sxs-lookup"><span data-stu-id="a6510-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="a6510-108">Hvis du vil behandle godkjenningen av et avvik, må brukeren som kjører oppgaveregistreringen ha en "Navn"-verdi som er tilordnet på siden Brukere.</span><span class="sxs-lookup"><span data-stu-id="a6510-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="a6510-109">Hvis du vil bruke merknader i dokumentet, må brukeren også ha Dokumenthåndtering aktivert i brukeralternativene.</span><span class="sxs-lookup"><span data-stu-id="a6510-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="a6510-110">Velge en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="a6510-110">Select a quality order</span></span>
1. <span data-ttu-id="a6510-111">I navigasjonsruten går du til **Moduler > Lagerstyring > Periodiske oppgaver > Kvalitetsstyring > Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a6510-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="a6510-112">I listen velger du kvalitetsordren som ble opprettet i [Kontrollere varekvaliteten](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="a6510-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="a6510-113">Opprette et avvik</span><span class="sxs-lookup"><span data-stu-id="a6510-113">Create a nonconformance</span></span>
1. <span data-ttu-id="a6510-114">Velg **Forespørsler** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a6510-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="a6510-115">Velg **Avvik**.</span><span class="sxs-lookup"><span data-stu-id="a6510-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="a6510-116">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a6510-116">Select **New**.</span></span>
4. <span data-ttu-id="a6510-117">Velg problemet som ble funnet under inspeksjonen, i rullegardinmenyen for **Problemtype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a6510-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="a6510-118">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6510-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="a6510-119">Godkjenne/avvise et avvik</span><span class="sxs-lookup"><span data-stu-id="a6510-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="a6510-120">Velg **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="a6510-120">Select **Functions**.</span></span>
2. <span data-ttu-id="a6510-121">Velg **Godkjenn avvik**.</span><span class="sxs-lookup"><span data-stu-id="a6510-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="a6510-122">Godkjenn avviket for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="a6510-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="a6510-123">Godkjente avvik kan knyttes til relaterte operasjoner for å registrere arbeid som utføres som en del av avvikshåndtering og, som i dette emnet, behandling av rettelseshandlingen.</span><span class="sxs-lookup"><span data-stu-id="a6510-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="a6510-124">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a6510-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="a6510-125">Opprette en rettelseshandling</span><span class="sxs-lookup"><span data-stu-id="a6510-125">Create a correction action</span></span>
1. <span data-ttu-id="a6510-126">Velg **Rettelser**.</span><span class="sxs-lookup"><span data-stu-id="a6510-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="a6510-127">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a6510-127">Select **New**.</span></span>
3. <span data-ttu-id="a6510-128">I **Personalnummer**-feltet i den nye raden velger du ønsket post fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="a6510-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="a6510-129">Klikk på **Velg**.</span><span class="sxs-lookup"><span data-stu-id="a6510-129">Click **Select**.</span></span>
5. <span data-ttu-id="a6510-130">Velg **Legg ved**.</span><span class="sxs-lookup"><span data-stu-id="a6510-130">Select **Attach**.</span></span> <span data-ttu-id="a6510-131">Opprett en merknad om rettelsen.</span><span class="sxs-lookup"><span data-stu-id="a6510-131">Create a note about the correction.</span></span> <span data-ttu-id="a6510-132">I dette eksemplet er handlingen å kontakte leverandøren for å diskutere avvikssaken.</span><span class="sxs-lookup"><span data-stu-id="a6510-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="a6510-133">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a6510-133">Select **New**.</span></span>
7. <span data-ttu-id="a6510-134">Velg **Notat**.</span><span class="sxs-lookup"><span data-stu-id="a6510-134">Select **Note**.</span></span> <span data-ttu-id="a6510-135">Avhengig av oppsettet for rapporten kan ulike dokumenttyper skrives ut på rapporter som er knyttet til behandling av avvik.</span><span class="sxs-lookup"><span data-stu-id="a6510-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="a6510-136">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a6510-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="a6510-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a6510-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="a6510-138">Vedlikeholde en korreksjon</span><span class="sxs-lookup"><span data-stu-id="a6510-138">Maintain a correction</span></span>
1. <span data-ttu-id="a6510-139">Velg **Merk som fullført**.</span><span class="sxs-lookup"><span data-stu-id="a6510-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="a6510-140">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6510-140">Select **OK**.</span></span>
3. <span data-ttu-id="a6510-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a6510-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="a6510-142">Lukke et avvik</span><span class="sxs-lookup"><span data-stu-id="a6510-142">Close a nonconformance</span></span>
1. <span data-ttu-id="a6510-143">Velg **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="a6510-143">Select **Functions**.</span></span>
2. <span data-ttu-id="a6510-144">Velg **Lukk avvik**.</span><span class="sxs-lookup"><span data-stu-id="a6510-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="a6510-145">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a6510-145">Select **Yes**.</span></span>
4. <span data-ttu-id="a6510-146">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="a6510-146">Close the pages.</span></span>
