--- 
title: "Utforme konfigurasjoner for å generere dokumenter med programdata"
description: "For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren \"ER generere dokumenter med oppdatering av programdata (del 1: importere konfigurasjoner)\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8376107a33dd83e04f82fcab6847e7f073f08dbc
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="63064-103">Utforme konfigurasjoner for å generere dokumenter med programdata</span><span class="sxs-lookup"><span data-stu-id="63064-103">Design configurations to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63064-104">For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 1: importere konfigurasjoner)".</span><span class="sxs-lookup"><span data-stu-id="63064-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="63064-105">Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="63064-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="63064-106">I denne prosedyren skal du kjøre den ER-importerte formatkonfigurasjonen som er opprettet for eksempelfirmaet Litware, Inc. for å generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="63064-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="63064-107">Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler.</span><span class="sxs-lookup"><span data-stu-id="63064-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="63064-108">Disse trinnene kan fullføres ved hjelp av DEMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="63064-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="63064-109">Før du begynner, må du endre land konteksten for firmaets DEMF fra DEU (Tyskland) til BEL (Belgia).</span><span class="sxs-lookup"><span data-stu-id="63064-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="63064-110">Klikk Organisasjonsadministrasjon > Organisasjoner > Juridiske enheter for å oppdatere landkoden i primæradressen for den juridiske enheten DEMF.</span><span class="sxs-lookup"><span data-stu-id="63064-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="63064-111">Start programmet på nytt.</span><span class="sxs-lookup"><span data-stu-id="63064-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="63064-112">Kjør importert ER-format</span><span class="sxs-lookup"><span data-stu-id="63064-112">Run imported ER format</span></span>
1. <span data-ttu-id="63064-113">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="63064-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="63064-114">Utvid 'Intrastat (modell)' i treet.</span><span class="sxs-lookup"><span data-stu-id="63064-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="63064-115">Velg 'Intrastat (modell)\Intrastat (format)' i treet.</span><span class="sxs-lookup"><span data-stu-id="63064-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="63064-116">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="63064-116">Click Run.</span></span>
    * <span data-ttu-id="63064-117">Kjør utkastversjonen av formatkonfigurasjonen ER å generere Intrastat-rapporten.</span><span class="sxs-lookup"><span data-stu-id="63064-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="63064-118">Skriv inn 'intrastat.xml' i feltet Angi filnavn.</span><span class="sxs-lookup"><span data-stu-id="63064-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="63064-119">Angi navnet på filen.</span><span class="sxs-lookup"><span data-stu-id="63064-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="63064-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="63064-120">Click OK.</span></span>
    * <span data-ttu-id="63064-121">Se gjennom den genererte XML-filen.</span><span class="sxs-lookup"><span data-stu-id="63064-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="63064-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="63064-122">Close the page.</span></span>
8. <span data-ttu-id="63064-123">Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="63064-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="63064-124">Åpmne dette skjemaet for å vise Intrastat-transaksjonene som er inkludert i det genererte elektroniske dokumentet.</span><span class="sxs-lookup"><span data-stu-id="63064-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="63064-125">Klikk Intrastat-arkiv.</span><span class="sxs-lookup"><span data-stu-id="63064-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="63064-126">Fordi det utførte ER-fomatet ikke inneholder innstillinger for oppdatering av programdata, ble detaljer om den fullførte Intrastat-rapporten ikke arkivert.</span><span class="sxs-lookup"><span data-stu-id="63064-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="63064-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="63064-127">Close the page.</span></span>
11. <span data-ttu-id="63064-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="63064-128">Close the page.</span></span>


