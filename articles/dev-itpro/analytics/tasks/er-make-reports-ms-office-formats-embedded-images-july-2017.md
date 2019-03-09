---
title: Utforme konfigurasjoner for å generere rapporter i Office-format med innebygde bilder
description: Fremgangsmåten i dette emnet viser hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner som genererer elektroniske dokumenter i Microsoft Office-formater (Excel og Word) som inneholder innebygde bilder.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fb02e561f6792c57b924ba64a5ca3d3974289ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "358100"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="c1a48-103">Utforme konfigurasjoner for å generere rapporter i Office-format med innebygde bilder</span><span class="sxs-lookup"><span data-stu-id="c1a48-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1a48-104">For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren "ER Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="c1a48-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="c1a48-105">Denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et Microsoft Excel- eller Microsoft Word-dokument som inneholder innebygde bilder.</span><span class="sxs-lookup"><span data-stu-id="c1a48-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="c1a48-106">I denne prosedyren skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet, Litware, Inc. Disse trinnene kan fullføres ved å bruke USMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="c1a48-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="c1a48-107">Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler.</span><span class="sxs-lookup"><span data-stu-id="c1a48-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c1a48-108">Før du begynner må du laste ned og lagre filene oppført i hjelpeemnet [Bygge inn bilder og figurer i forretningsdokumenter som blir generert ved hjelp av verktøyet for elektronisk rapportering](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="c1a48-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in business documents that are generated with the Electronic reporting tool](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="c1a48-109">Filene er: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png og Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="c1a48-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="c1a48-110">Kontrollere forhåndskrav</span><span class="sxs-lookup"><span data-stu-id="c1a48-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="c1a48-111">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="c1a48-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="c1a48-112">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="c1a48-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c1a48-113">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="c1a48-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="c1a48-114">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="c1a48-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="c1a48-115">Legg til en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="c1a48-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="c1a48-116">I stedet for å opprette en ny modell kan du laste ER-modellkonfigurasjonsfilen (modell for cheques.xml) som du lagret tidligere.</span><span class="sxs-lookup"><span data-stu-id="c1a48-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="c1a48-117">Denne filen inneholder eksempeldatamodellen for betalingssjekker og tilordningen av datamodellen til datakomponentene i Dynamics 365 for Operations-programmet.</span><span class="sxs-lookup"><span data-stu-id="c1a48-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="c1a48-118">Klikk Veksle på hurtigfanen Versjoner.</span><span class="sxs-lookup"><span data-stu-id="c1a48-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="c1a48-119">Klikk Last fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="c1a48-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c1a48-120">Klikk Bla gjennom, og velg deretter Modell for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="c1a48-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="c1a48-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c1a48-121">Click OK.</span></span>  
 6. <span data-ttu-id="c1a48-122">Den lastede modellen brukes som en datakilde med informasjon for å generere dokumenter som inneholder bilder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="c1a48-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="c1a48-123">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="c1a48-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="c1a48-124">I stedet for å opprette et nytt format kan du laste ER-formatkonfigurasjonsfilen (Cheques printing format.xml) som du lagret tidligere.</span><span class="sxs-lookup"><span data-stu-id="c1a48-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="c1a48-125">Denne filen inneholder eksempelutformingen på formatet for å skrive ut sjekker ved hjelp av det forhåndstrykte skjemaet og tilordningen av dette formatet til "Modell for sjekker"-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="c1a48-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="c1a48-126">Klikk Veksle.</span><span class="sxs-lookup"><span data-stu-id="c1a48-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="c1a48-127">Klikk Last fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="c1a48-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c1a48-128">Klikk Bla gjennom og velg Cheques printing format.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="c1a48-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="c1a48-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c1a48-129">Click OK.</span></span>  
 6. <span data-ttu-id="c1a48-130">Utvid Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="c1a48-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="c1a48-131">Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="c1a48-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="c1a48-132">Det lastede formatet brukes for å generere dokumenter som inneholder bilder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="c1a48-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="c1a48-133">Konfigurere ER-brukerparametere</span><span class="sxs-lookup"><span data-stu-id="c1a48-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="c1a48-134">Klikk Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c1a48-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="c1a48-135">Klikk Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="c1a48-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="c1a48-136">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="c1a48-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="c1a48-137">Aktiver flagget Kjøringsutkast for å starte utkastversjonen av det valgte formatet i stedet for den fullførte.</span><span class="sxs-lookup"><span data-stu-id="c1a48-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="c1a48-138">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c1a48-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="c1a48-139">Konfigurere Parametere for kontant- og bankbehandling</span><span class="sxs-lookup"><span data-stu-id="c1a48-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="c1a48-140">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="c1a48-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="c1a48-141">Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="c1a48-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="c1a48-142">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c1a48-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="c1a48-143">Klikk Kontroller.</span><span class="sxs-lookup"><span data-stu-id="c1a48-143">Click Check.</span></span>  
 5. <span data-ttu-id="c1a48-144">Utvid Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="c1a48-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="c1a48-145">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="c1a48-145">Click Edit.</span></span>  
 7. <span data-ttu-id="c1a48-146">Velg Ja i Firmalogo-feltet.</span><span class="sxs-lookup"><span data-stu-id="c1a48-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="c1a48-147">Klikk på Firmalogo.</span><span class="sxs-lookup"><span data-stu-id="c1a48-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="c1a48-148">Klikk Endre.</span><span class="sxs-lookup"><span data-stu-id="c1a48-148">Click Change.</span></span>  
 10. <span data-ttu-id="c1a48-149">Klikk Bla gjennom og velg filen du lastet ned tidligere, Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="c1a48-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="c1a48-150">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c1a48-150">Click Save.</span></span>  
 12. <span data-ttu-id="c1a48-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1a48-151">Close the page.</span></span>  
 13. <span data-ttu-id="c1a48-152">Utvid seksjonen Signatur.</span><span class="sxs-lookup"><span data-stu-id="c1a48-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="c1a48-153">Velg Ja i feltet Skriv ut første signatur.</span><span class="sxs-lookup"><span data-stu-id="c1a48-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="c1a48-154">Klikk Endre.</span><span class="sxs-lookup"><span data-stu-id="c1a48-154">Click Change.</span></span>  
 16. <span data-ttu-id="c1a48-155">Klikk Bla gjennom og velg filen du lastet ned tidligere, Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="c1a48-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="c1a48-156">Utvid Kopier-seksjonen.</span><span class="sxs-lookup"><span data-stu-id="c1a48-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="c1a48-157">Velg et alternativ i feltet Vannmerke.</span><span class="sxs-lookup"><span data-stu-id="c1a48-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="c1a48-158">Velg Ja i feltet Generelt elektronisk eksportformat.</span><span class="sxs-lookup"><span data-stu-id="c1a48-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="c1a48-159">Velg Cheques printing form-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="c1a48-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="c1a48-160">Nå brukes det valgte ER-formatet for utskrift av sjekker.</span><span class="sxs-lookup"><span data-stu-id="c1a48-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="c1a48-161">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="c1a48-161">Click Attach.</span></span>  
 23. <span data-ttu-id="c1a48-162">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c1a48-162">Click New.</span></span>  
 24. <span data-ttu-id="c1a48-163">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="c1a48-163">Click File.</span></span>  
 25. <span data-ttu-id="c1a48-164">Klikk Bla gjennom og velg filen du lastet ned tidligere, Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="c1a48-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="c1a48-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1a48-165">Close the page.</span></span>  
 27. <span data-ttu-id="c1a48-166">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1a48-166">Close the page.</span></span>  
 28. <span data-ttu-id="c1a48-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1a48-167">Close the page.</span></span>  
 29. <span data-ttu-id="c1a48-168">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="c1a48-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="c1a48-169">Velg Ja i feltet Tillat oppretting av forhåndsmerknader for inaktive bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="c1a48-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="c1a48-170">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c1a48-170">Click Save.</span></span>  
 32. <span data-ttu-id="c1a48-171">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1a48-171">Close the page.</span></span>  
