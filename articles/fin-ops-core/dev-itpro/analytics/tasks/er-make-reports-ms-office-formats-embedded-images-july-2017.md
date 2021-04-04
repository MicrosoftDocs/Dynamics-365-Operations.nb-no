---
title: Utforme konfigurasjoner for å generere rapporter i Office-format med innebygde bilder
description: Dette emnet beskriver hvordan du utformer konfigurasjoner som genererer elektroniske dokumenter i Excel- og Word-formater som inneholder innebygde bilder.
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: 3585d99ce2db8a7833b11a4bcc68f9e91023b9cd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569491"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="cf6ed-103">Utforme konfigurasjoner for å generere rapporter i Office-format med innebygde bilder</span><span class="sxs-lookup"><span data-stu-id="cf6ed-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf6ed-104">For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren "ER Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="cf6ed-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="cf6ed-105">Denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et Microsoft Excel- eller Word-dokument som inneholder innebygde bilder.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="cf6ed-106">I denne prosedyren skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet, Litware, Inc. Disse trinnene kan fullføres ved å bruke USMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="cf6ed-107">Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="cf6ed-108">Før du begynner må du laste ned og lagre filene oppført i hjelpeemnet [Bygge inn bilder og figurer i forretningsdokumenter som blir generert ved hjelp av ER](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="cf6ed-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="cf6ed-109">Filene er: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png og Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="cf6ed-110">Kontrollere forhåndskrav</span><span class="sxs-lookup"><span data-stu-id="cf6ed-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="cf6ed-111">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="cf6ed-112">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="cf6ed-113">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="cf6ed-113">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="cf6ed-114">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="cf6ed-115">Legg til en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="cf6ed-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="cf6ed-116">I stedet for å opprette en ny modell kan du laste ER-modellkonfigurasjonsfilen (modell for cheques.xml) som du lagret tidligere.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="cf6ed-117">Denne filen inneholder eksempeldatamodellen for betalingssjekker og tilordningen av datamodellen til datakomponentene i Dynamics 365 for Operations-programmet.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="cf6ed-118">Klikk Veksle på hurtigfanen Versjoner.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="cf6ed-119">Klikk på Last fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="cf6ed-120">Klikk på Bla gjennom, og velg deretter Modell for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="cf6ed-121">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-121">Click OK.</span></span>  
 6. <span data-ttu-id="cf6ed-122">Den lastede modellen brukes som en datakilde med informasjon for å generere dokumenter som inneholder bilder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="cf6ed-123">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="cf6ed-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="cf6ed-124">I stedet for å opprette et nytt format kan du laste ER-formatkonfigurasjonsfilen (Cheques printing format.xml) som du lagret tidligere.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="cf6ed-125">Denne filen inneholder eksempelutformingen på formatet for å skrive ut sjekker ved hjelp av det forhåndstrykte skjemaet og tilordningen av dette formatet til "Modell for sjekker"-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="cf6ed-126">Klikk på Veksle.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="cf6ed-127">Klikk på Last fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="cf6ed-128">Klikk på Bla gjennom og velg Cheques printing format.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="cf6ed-129">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-129">Click OK.</span></span>  
 6. <span data-ttu-id="cf6ed-130">Utvid Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="cf6ed-131">Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="cf6ed-132">Det lastede formatet brukes for å generere dokumenter som inneholder bilder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="cf6ed-133">Konfigurere ER-brukerparametere</span><span class="sxs-lookup"><span data-stu-id="cf6ed-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="cf6ed-134">Klikk på Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="cf6ed-135">Klikk på Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="cf6ed-136">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="cf6ed-137">Aktiver flagget Kjøringsutkast for å starte utkastversjonen av det valgte formatet i stedet for den fullførte.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-137">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="cf6ed-138">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="cf6ed-139">Konfigurere Parametere for kontant- og bankbehandling</span><span class="sxs-lookup"><span data-stu-id="cf6ed-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="cf6ed-140">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="cf6ed-141">Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="cf6ed-142">Klikk på Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="cf6ed-143">Klikk på Kontroller.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-143">Click Check.</span></span>  
 5. <span data-ttu-id="cf6ed-144">Utvid Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="cf6ed-145">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-145">Click Edit.</span></span>  
 7. <span data-ttu-id="cf6ed-146">Velg Ja i Firmalogo-feltet.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="cf6ed-147">Klikk på Firmalogo.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="cf6ed-148">Klikk på Endre.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-148">Click Change.</span></span>  
 10. <span data-ttu-id="cf6ed-149">Klikk på Bla gjennom og velg filen du lastet ned tidligere, Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="cf6ed-150">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-150">Click Save.</span></span>  
 12. <span data-ttu-id="cf6ed-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-151">Close the page.</span></span>  
 13. <span data-ttu-id="cf6ed-152">Utvid seksjonen Signatur.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="cf6ed-153">Velg Ja i feltet Skriv ut første signatur.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="cf6ed-154">Klikk på Endre.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-154">Click Change.</span></span>  
 16. <span data-ttu-id="cf6ed-155">Klikk på Bla gjennom og velg filen du lastet ned tidligere, Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="cf6ed-156">Utvid Kopier-seksjonen.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="cf6ed-157">Velg et alternativ i feltet Vannmerke.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="cf6ed-158">Velg Ja i feltet Generelt elektronisk eksportformat.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="cf6ed-159">Velg Cheques printing form-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="cf6ed-160">Nå brukes det valgte ER-formatet for utskrift av sjekker.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="cf6ed-161">Klikk på Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-161">Click Attach.</span></span>  
 23. <span data-ttu-id="cf6ed-162">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-162">Click New.</span></span>  
 24. <span data-ttu-id="cf6ed-163">Klikk på Fil.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-163">Click File.</span></span>  
 25. <span data-ttu-id="cf6ed-164">Klikk på Bla gjennom og velg filen du lastet ned tidligere, Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="cf6ed-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-165">Close the page.</span></span>  
 27. <span data-ttu-id="cf6ed-166">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-166">Close the page.</span></span>  
 28. <span data-ttu-id="cf6ed-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-167">Close the page.</span></span>  
 29. <span data-ttu-id="cf6ed-168">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="cf6ed-169">Velg Ja i feltet Tillat oppretting av forhåndsmerknader for inaktive bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="cf6ed-170">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-170">Click Save.</span></span>  
 32. <span data-ttu-id="cf6ed-171">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-171">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]