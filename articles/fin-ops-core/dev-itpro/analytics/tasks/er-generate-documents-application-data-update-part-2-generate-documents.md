---
title: Utforme konfigurasjoner for å generere dokumenter med programdata
description: Dette emnet beskriver hvordan du utformer konfigurasjoner for elektronisk rapportering (ER) for å generere et elektronisk dokument. (Del 1 – importere konfigurasjoner).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 417c419dc6925bac337fe74a2f057395316ec75d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092928"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="c36e0-104">Utforme konfigurasjoner for å generere dokumenter med programdata</span><span class="sxs-lookup"><span data-stu-id="c36e0-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c36e0-105">For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 1: importere konfigurasjoner)".</span><span class="sxs-lookup"><span data-stu-id="c36e0-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="c36e0-106">Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="c36e0-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="c36e0-107">I denne prosedyren skal du kjøre den ER-importerte formatkonfigurasjonen som er opprettet for eksempelfirmaet Litware, Inc. for å generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="c36e0-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="c36e0-108">Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler.</span><span class="sxs-lookup"><span data-stu-id="c36e0-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c36e0-109">Disse trinnene kan fullføres ved hjelp av DEMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="c36e0-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="c36e0-110">Før du begynner, må du endre land konteksten for firmaets DEMF fra DEU (Tyskland) til BEL (Belgia).</span><span class="sxs-lookup"><span data-stu-id="c36e0-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="c36e0-111">Klikk på Organisasjonsadministrasjon > Organisasjoner > Juridiske enheter for å oppdatere landkoden i primæradressen for den juridiske enheten DEMF.</span><span class="sxs-lookup"><span data-stu-id="c36e0-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="c36e0-112">Start programmet på nytt.</span><span class="sxs-lookup"><span data-stu-id="c36e0-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="c36e0-113">Kjør importert ER-format</span><span class="sxs-lookup"><span data-stu-id="c36e0-113">Run imported ER format</span></span>
1. <span data-ttu-id="c36e0-114">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="c36e0-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c36e0-115">Utvid 'Intrastat (modell)' i treet.</span><span class="sxs-lookup"><span data-stu-id="c36e0-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="c36e0-116">Velg 'Intrastat (modell)\Intrastat (format)' i treet.</span><span class="sxs-lookup"><span data-stu-id="c36e0-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="c36e0-117">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="c36e0-117">Click Run.</span></span>
    * <span data-ttu-id="c36e0-118">Kjør utkastversjonen av formatkonfigurasjonen ER å generere Intrastat-rapporten.</span><span class="sxs-lookup"><span data-stu-id="c36e0-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="c36e0-119">Skriv inn 'intrastat.xml' i feltet Angi filnavn.</span><span class="sxs-lookup"><span data-stu-id="c36e0-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="c36e0-120">Angi navnet på filen.</span><span class="sxs-lookup"><span data-stu-id="c36e0-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="c36e0-121">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="c36e0-121">Click OK.</span></span>
    * <span data-ttu-id="c36e0-122">Se gjennom den genererte XML-filen.</span><span class="sxs-lookup"><span data-stu-id="c36e0-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="c36e0-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c36e0-123">Close the page.</span></span>
8. <span data-ttu-id="c36e0-124">Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="c36e0-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="c36e0-125">Åpmne dette skjemaet for å vise Intrastat-transaksjonene som er inkludert i det genererte elektroniske dokumentet.</span><span class="sxs-lookup"><span data-stu-id="c36e0-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="c36e0-126">Klikk på Intrastat-arkiv.</span><span class="sxs-lookup"><span data-stu-id="c36e0-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="c36e0-127">Fordi det utførte ER-fomatet ikke inneholder innstillinger for oppdatering av programdata, ble detaljer om den fullførte Intrastat-rapporten ikke arkivert.</span><span class="sxs-lookup"><span data-stu-id="c36e0-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="c36e0-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c36e0-128">Close the page.</span></span>
11. <span data-ttu-id="c36e0-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c36e0-129">Close the page.</span></span>

