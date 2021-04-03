---
title: Generere dokumenter som inneholder programdata
description: 'For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 4: endre format)".'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c474f4bc7940a429ed62870e00302c93581eb9a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569587"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="30b27-103">Generere dokumenter som inneholder programdata</span><span class="sxs-lookup"><span data-stu-id="30b27-103">Generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30b27-104">For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 4: endre format)".</span><span class="sxs-lookup"><span data-stu-id="30b27-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 4: Modify format)".</span></span>



<span data-ttu-id="30b27-105">Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument og oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="30b27-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="30b27-106">I denne prosedyren, kan du utføre ER-formatkonfigurasjonen for å generere Intrastat-rapporten og oppdatere programdata for arkivering detaljer om rapporteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="30b27-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="30b27-107">Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler.</span><span class="sxs-lookup"><span data-stu-id="30b27-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="30b27-108">Disse trinnene kan fullføres ved hjelp av DEMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="30b27-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="30b27-109">Før du begynner, kontroller at konteksten for firmaets DEMF land er BEL (Belgia).</span><span class="sxs-lookup"><span data-stu-id="30b27-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="30b27-110">Angi utenrikshandelsparametere</span><span class="sxs-lookup"><span data-stu-id="30b27-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="30b27-111">Gå til Avgift > Oppsett > Utenrikshandel > Utenrikshandelsparametere.</span><span class="sxs-lookup"><span data-stu-id="30b27-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="30b27-112">Klikk kategorien Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="30b27-112">Click the Number sequences tab.</span></span>

    <span data-ttu-id="30b27-113">Arkiverer detaljer om Intrastat-rapporteringsprosessen. Vi må identifisere poster i hvert arkiv vi har opprettet.</span><span class="sxs-lookup"><span data-stu-id="30b27-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="30b27-114">En bestemt nummerserie må konfigureres for dette.</span><span class="sxs-lookup"><span data-stu-id="30b27-114">A special number sequence must be configured for that.</span></span>  

3. <span data-ttu-id="30b27-115">Velg referansen "ID for Intrastat-arkiv".</span><span class="sxs-lookup"><span data-stu-id="30b27-115">Select the 'Intrastat archive ID' reference.</span></span>
4. <span data-ttu-id="30b27-116">Skriv inn en verdi i feltet Nummerserie.</span><span class="sxs-lookup"><span data-stu-id="30b27-116">In the Number sequence code field, type a value.</span></span>

    <span data-ttu-id="30b27-117">Angi eller velg verdien "Fore_2" i Nummerseriekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="30b27-117">In the 'Number sequence code' field, enter or select the value 'Fore_2'.</span></span>  

5. <span data-ttu-id="30b27-118">ResolveChanges nummerseriekoden.</span><span class="sxs-lookup"><span data-stu-id="30b27-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="30b27-119">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="30b27-119">Click Save.</span></span>
7. <span data-ttu-id="30b27-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="30b27-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="30b27-121">Kjør modifisert ER-format</span><span class="sxs-lookup"><span data-stu-id="30b27-121">Run modified ER format</span></span>
1. <span data-ttu-id="30b27-122">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="30b27-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="30b27-123">Utvid 'Intrastat (modell)' i treet.</span><span class="sxs-lookup"><span data-stu-id="30b27-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="30b27-124">Velg 'Intrastat (modell)\Intrastat (format)' i treet.</span><span class="sxs-lookup"><span data-stu-id="30b27-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="30b27-125">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="30b27-125">Click Run.</span></span>
5. <span data-ttu-id="30b27-126">Skriv inn 'intrastat2.xml' i feltet Angi filnavn.</span><span class="sxs-lookup"><span data-stu-id="30b27-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
6. <span data-ttu-id="30b27-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="30b27-127">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="30b27-128">Gå gjennom resultatene av kjøringen av ER-formatet</span><span class="sxs-lookup"><span data-stu-id="30b27-128">Review ER format execution's results</span></span>
<span data-ttu-id="30b27-129">Se gjennom den genererte XML-filen.</span><span class="sxs-lookup"><span data-stu-id="30b27-129">Review the generated XML file.</span></span>  
1. <span data-ttu-id="30b27-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="30b27-130">Close the page.</span></span>
2. <span data-ttu-id="30b27-131">Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="30b27-131">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>

    <span data-ttu-id="30b27-132">Åpmne dette skjemaet med Intrastat-transaksjoner som er inkludert i det genererte elektroniske dokumentet.</span><span class="sxs-lookup"><span data-stu-id="30b27-132">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  

3. <span data-ttu-id="30b27-133">Klikk Intrastat-arkiv.</span><span class="sxs-lookup"><span data-stu-id="30b27-133">Click Intrastat archive.</span></span>

    <span data-ttu-id="30b27-134">Siden det utførte ER-formatet må inneholder innstillinger for oppdatering av programdata, ble detaljer om den fullførte Intrastat-rapporten arkivert.</span><span class="sxs-lookup"><span data-stu-id="30b27-134">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="30b27-135">I dette skjemaet kan du se hovedposten for det opprettede arkivet.</span><span class="sxs-lookup"><span data-stu-id="30b27-135">In this form, you can see the header record of the created archive.</span></span>  

4. <span data-ttu-id="30b27-136">Klikk Detaljer.</span><span class="sxs-lookup"><span data-stu-id="30b27-136">Click Details.</span></span>

    <span data-ttu-id="30b27-137">I dette skjemaet kan du se detaljene for det opprettede arkivet.</span><span class="sxs-lookup"><span data-stu-id="30b27-137">In this form, you can see the details for the created archive.</span></span>  

5. <span data-ttu-id="30b27-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="30b27-138">Close the page.</span></span>
6. <span data-ttu-id="30b27-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="30b27-139">Close the page.</span></span>
7. <span data-ttu-id="30b27-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="30b27-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]