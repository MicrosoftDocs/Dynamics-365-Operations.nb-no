---
title: Utforme konfigurasjoner for å generere rapporter i Office-format med innebygde bilder
description: Dette emnet beskriver hvordan du utformer konfigurasjoner som genererer elektroniske dokumenter i Excel- og Word-formater som inneholder innebygde bilder.
author: NickSelin
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1bafc919d73c9e603935398563bb26e8fb277d3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751064"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="55626-103">Utforme konfigurasjoner for å generere rapporter i Office-format med innebygde bilder</span><span class="sxs-lookup"><span data-stu-id="55626-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55626-104">For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren "ER Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="55626-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="55626-105">Denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et Microsoft Excel- eller Word-dokument som inneholder innebygde bilder.</span><span class="sxs-lookup"><span data-stu-id="55626-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="55626-106">I denne prosedyren skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet, Litware, Inc. Disse trinnene kan fullføres ved å bruke USMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="55626-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="55626-107">Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler.</span><span class="sxs-lookup"><span data-stu-id="55626-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="55626-108">Før du begynner må du laste ned og lagre filene oppført i hjelpeemnet [Bygge inn bilder og figurer i forretningsdokumenter som blir generert ved hjelp av ER](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="55626-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="55626-109">Filene er: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png og Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="55626-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="55626-110">Kontrollere forhåndskrav</span><span class="sxs-lookup"><span data-stu-id="55626-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="55626-111">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="55626-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="55626-112">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="55626-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="55626-113">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="55626-113">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="55626-114">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="55626-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="55626-115">Legg til en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="55626-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="55626-116">I stedet for å opprette en ny modell kan du laste ER-modellkonfigurasjonsfilen (modell for cheques.xml) som du lagret tidligere.</span><span class="sxs-lookup"><span data-stu-id="55626-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="55626-117">Denne filen inneholder eksempeldatamodellen for betalingssjekker og tilordningen av datamodellen til datakomponentene i Dynamics 365 for Operations-programmet.</span><span class="sxs-lookup"><span data-stu-id="55626-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="55626-118">Klikk Veksle på hurtigfanen Versjoner.</span><span class="sxs-lookup"><span data-stu-id="55626-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="55626-119">Klikk på Last fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="55626-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="55626-120">Klikk på Bla gjennom, og velg deretter Modell for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="55626-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="55626-121">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="55626-121">Click OK.</span></span>  
 6. <span data-ttu-id="55626-122">Den lastede modellen brukes som en datakilde med informasjon for å generere dokumenter som inneholder bilder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="55626-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="55626-123">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="55626-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="55626-124">I stedet for å opprette et nytt format kan du laste ER-formatkonfigurasjonsfilen (Cheques printing format.xml) som du lagret tidligere.</span><span class="sxs-lookup"><span data-stu-id="55626-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="55626-125">Denne filen inneholder eksempelutformingen på formatet for å skrive ut sjekker ved hjelp av det forhåndstrykte skjemaet og tilordningen av dette formatet til "Modell for sjekker"-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="55626-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="55626-126">Klikk på Veksle.</span><span class="sxs-lookup"><span data-stu-id="55626-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="55626-127">Klikk på Last fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="55626-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="55626-128">Klikk på Bla gjennom og velg Cheques printing format.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="55626-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="55626-129">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="55626-129">Click OK.</span></span>  
 6. <span data-ttu-id="55626-130">Utvid Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="55626-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="55626-131">Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="55626-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="55626-132">Det lastede formatet brukes for å generere dokumenter som inneholder bilder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="55626-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="55626-133">Konfigurere ER-brukerparametere</span><span class="sxs-lookup"><span data-stu-id="55626-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="55626-134">Klikk på Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="55626-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="55626-135">Klikk på Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="55626-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="55626-136">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="55626-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="55626-137">Aktiver flagget Kjøringsutkast for å starte utkastversjonen av det valgte formatet i stedet for den fullførte.</span><span class="sxs-lookup"><span data-stu-id="55626-137">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="55626-138">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="55626-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="55626-139">Konfigurere Parametere for kontant- og bankbehandling</span><span class="sxs-lookup"><span data-stu-id="55626-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="55626-140">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="55626-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="55626-141">Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="55626-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="55626-142">Klikk på Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="55626-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="55626-143">Klikk på Kontroller.</span><span class="sxs-lookup"><span data-stu-id="55626-143">Click Check.</span></span>  
 5. <span data-ttu-id="55626-144">Utvid Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="55626-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="55626-145">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="55626-145">Click Edit.</span></span>  
 7. <span data-ttu-id="55626-146">Velg Ja i Firmalogo-feltet.</span><span class="sxs-lookup"><span data-stu-id="55626-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="55626-147">Klikk på Firmalogo.</span><span class="sxs-lookup"><span data-stu-id="55626-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="55626-148">Klikk på Endre.</span><span class="sxs-lookup"><span data-stu-id="55626-148">Click Change.</span></span>  
 10. <span data-ttu-id="55626-149">Klikk på Bla gjennom og velg filen du lastet ned tidligere, Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="55626-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="55626-150">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="55626-150">Click Save.</span></span>  
 12. <span data-ttu-id="55626-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="55626-151">Close the page.</span></span>  
 13. <span data-ttu-id="55626-152">Utvid seksjonen Signatur.</span><span class="sxs-lookup"><span data-stu-id="55626-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="55626-153">Velg Ja i feltet Skriv ut første signatur.</span><span class="sxs-lookup"><span data-stu-id="55626-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="55626-154">Klikk på Endre.</span><span class="sxs-lookup"><span data-stu-id="55626-154">Click Change.</span></span>  
 16. <span data-ttu-id="55626-155">Klikk på Bla gjennom og velg filen du lastet ned tidligere, Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="55626-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="55626-156">Utvid Kopier-seksjonen.</span><span class="sxs-lookup"><span data-stu-id="55626-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="55626-157">Velg et alternativ i feltet Vannmerke.</span><span class="sxs-lookup"><span data-stu-id="55626-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="55626-158">Velg Ja i feltet Generelt elektronisk eksportformat.</span><span class="sxs-lookup"><span data-stu-id="55626-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="55626-159">Velg Cheques printing form-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="55626-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="55626-160">Nå brukes det valgte ER-formatet for utskrift av sjekker.</span><span class="sxs-lookup"><span data-stu-id="55626-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="55626-161">Klikk på Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="55626-161">Click Attach.</span></span>  
 23. <span data-ttu-id="55626-162">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="55626-162">Click New.</span></span>  
 24. <span data-ttu-id="55626-163">Klikk på Fil.</span><span class="sxs-lookup"><span data-stu-id="55626-163">Click File.</span></span>  
 25. <span data-ttu-id="55626-164">Klikk på Bla gjennom og velg filen du lastet ned tidligere, Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="55626-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="55626-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="55626-165">Close the page.</span></span>  
 27. <span data-ttu-id="55626-166">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="55626-166">Close the page.</span></span>  
 28. <span data-ttu-id="55626-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="55626-167">Close the page.</span></span>  
 29. <span data-ttu-id="55626-168">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="55626-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="55626-169">Velg Ja i feltet Tillat oppretting av forhåndsmerknader for inaktive bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="55626-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="55626-170">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="55626-170">Click Save.</span></span>  
 32. <span data-ttu-id="55626-171">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="55626-171">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]