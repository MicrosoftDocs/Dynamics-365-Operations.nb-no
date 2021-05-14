---
title: Utforme konfigurasjoner for å generere rapporter i Office-format med innebygde bilder
description: Dette emnet beskriver hvordan du utformer konfigurasjoner som genererer elektroniske dokumenter i Excel- og Word-formater som inneholder innebygde bilder.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944563"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="7f947-103">Utforme konfigurasjoner for å generere rapporter i Office-format med innebygde bilder</span><span class="sxs-lookup"><span data-stu-id="7f947-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f947-104">For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren "ER Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="7f947-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="7f947-105">Denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et Microsoft Excel- eller Word-dokument som inneholder innebygde bilder.</span><span class="sxs-lookup"><span data-stu-id="7f947-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="7f947-106">I denne prosedyren skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet, Litware, Inc. Disse trinnene kan fullføres ved å bruke USMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="7f947-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="7f947-107">Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler.</span><span class="sxs-lookup"><span data-stu-id="7f947-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="7f947-108">Før du starter kan du laste ned og lagre følgende filer:</span><span class="sxs-lookup"><span data-stu-id="7f947-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="7f947-109">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="7f947-109">Description</span></span>                                          | <span data-ttu-id="7f947-110">Filnavn</span><span class="sxs-lookup"><span data-stu-id="7f947-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="7f947-111">ER-datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="7f947-111">ER data model configuration</span></span>                          | [<span data-ttu-id="7f947-112">Modell for sjekker.xml</span><span class="sxs-lookup"><span data-stu-id="7f947-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="7f947-113">ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="7f947-113">ER format configuration</span></span>                              | [<span data-ttu-id="7f947-114">Utskriftsformat for sjekker.xml</span><span class="sxs-lookup"><span data-stu-id="7f947-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="7f947-115">Firmalogobilde</span><span class="sxs-lookup"><span data-stu-id="7f947-115">Company logo image</span></span>                                   | [<span data-ttu-id="7f947-116">Firmalogo.png</span><span class="sxs-lookup"><span data-stu-id="7f947-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="7f947-117">Signaturbilde</span><span class="sxs-lookup"><span data-stu-id="7f947-117">Signature image</span></span>                                      | [<span data-ttu-id="7f947-118">Signaturbilde.png</span><span class="sxs-lookup"><span data-stu-id="7f947-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="7f947-119">Alternativt signaturbilde</span><span class="sxs-lookup"><span data-stu-id="7f947-119">Alternative signature image</span></span>                          | [<span data-ttu-id="7f947-120">Signaturbilde 2.png</span><span class="sxs-lookup"><span data-stu-id="7f947-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="7f947-121">Microsoft Word-mal for utskrift av betalingssjekker</span><span class="sxs-lookup"><span data-stu-id="7f947-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="7f947-122">Sjekkmal Word.docx</span><span class="sxs-lookup"><span data-stu-id="7f947-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="7f947-123">Kontrollere forhåndskrav</span><span class="sxs-lookup"><span data-stu-id="7f947-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="7f947-124">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="7f947-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="7f947-125">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="7f947-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="7f947-126">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="7f947-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="7f947-127">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="7f947-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="7f947-128">Legg til en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="7f947-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="7f947-129">I stedet for å opprette en ny modell kan du laste ER-modellkonfigurasjonsfilen (modell for cheques.xml) som du lagret tidligere.</span><span class="sxs-lookup"><span data-stu-id="7f947-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="7f947-130">Denne filen inneholder eksempeldatamodellen for betalingssjekker og tilordningen av datamodellen til datakomponentene i Dynamics 365 for Operations-programmet.</span><span class="sxs-lookup"><span data-stu-id="7f947-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="7f947-131">Klikk Veksle på hurtigfanen Versjoner.</span><span class="sxs-lookup"><span data-stu-id="7f947-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="7f947-132">Klikk på Last fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="7f947-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="7f947-133">Klikk på Bla gjennom, og velg deretter Modell for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="7f947-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="7f947-134">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="7f947-134">Click OK.</span></span>  
 6. <span data-ttu-id="7f947-135">Den lastede modellen brukes som en datakilde med informasjon for å generere dokumenter som inneholder bilder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="7f947-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="7f947-136">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="7f947-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="7f947-137">I stedet for å opprette et nytt format kan du laste ER-formatkonfigurasjonsfilen (Cheques printing format.xml) som du lagret tidligere.</span><span class="sxs-lookup"><span data-stu-id="7f947-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="7f947-138">Denne filen inneholder eksempelutformingen på formatet for å skrive ut sjekker ved hjelp av det forhåndstrykte skjemaet og tilordningen av dette formatet til "Modell for sjekker"-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="7f947-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="7f947-139">Klikk på Veksle.</span><span class="sxs-lookup"><span data-stu-id="7f947-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="7f947-140">Klikk på Last fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="7f947-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="7f947-141">Klikk på Bla gjennom og velg Cheques printing format.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="7f947-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="7f947-142">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="7f947-142">Click OK.</span></span>  
 6. <span data-ttu-id="7f947-143">Utvid Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="7f947-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="7f947-144">Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f947-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="7f947-145">Det lastede formatet brukes for å generere dokumenter som inneholder bilder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="7f947-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="7f947-146">Konfigurere ER-brukerparametere</span><span class="sxs-lookup"><span data-stu-id="7f947-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="7f947-147">Klikk på Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7f947-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="7f947-148">Klikk på Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="7f947-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="7f947-149">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="7f947-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="7f947-150">Aktiver flagget Kjøringsutkast for å starte utkastversjonen av det valgte formatet i stedet for den fullførte.</span><span class="sxs-lookup"><span data-stu-id="7f947-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="7f947-151">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="7f947-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="7f947-152">Konfigurere Parametere for kontant- og bankbehandling</span><span class="sxs-lookup"><span data-stu-id="7f947-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="7f947-153">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="7f947-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="7f947-154">Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="7f947-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="7f947-155">Klikk på Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7f947-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="7f947-156">Klikk på Kontroller.</span><span class="sxs-lookup"><span data-stu-id="7f947-156">Click Check.</span></span>  
 5. <span data-ttu-id="7f947-157">Utvid Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="7f947-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="7f947-158">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="7f947-158">Click Edit.</span></span>  
 7. <span data-ttu-id="7f947-159">Velg Ja i Firmalogo-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f947-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="7f947-160">Klikk på Firmalogo.</span><span class="sxs-lookup"><span data-stu-id="7f947-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="7f947-161">Klikk på Endre.</span><span class="sxs-lookup"><span data-stu-id="7f947-161">Click Change.</span></span>  
 10. <span data-ttu-id="7f947-162">Klikk på Bla gjennom og velg filen du lastet ned tidligere, Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="7f947-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="7f947-163">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="7f947-163">Click Save.</span></span>  
 12. <span data-ttu-id="7f947-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f947-164">Close the page.</span></span>  
 13. <span data-ttu-id="7f947-165">Utvid seksjonen Signatur.</span><span class="sxs-lookup"><span data-stu-id="7f947-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="7f947-166">Velg Ja i feltet Skriv ut første signatur.</span><span class="sxs-lookup"><span data-stu-id="7f947-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="7f947-167">Klikk på Endre.</span><span class="sxs-lookup"><span data-stu-id="7f947-167">Click Change.</span></span>  
 16. <span data-ttu-id="7f947-168">Klikk på Bla gjennom og velg filen du lastet ned tidligere, Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="7f947-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="7f947-169">Utvid Kopier-seksjonen.</span><span class="sxs-lookup"><span data-stu-id="7f947-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="7f947-170">Velg et alternativ i feltet Vannmerke.</span><span class="sxs-lookup"><span data-stu-id="7f947-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="7f947-171">Velg Ja i feltet Generelt elektronisk eksportformat.</span><span class="sxs-lookup"><span data-stu-id="7f947-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="7f947-172">Velg Cheques printing form-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="7f947-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="7f947-173">Nå brukes det valgte ER-formatet for utskrift av sjekker.</span><span class="sxs-lookup"><span data-stu-id="7f947-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="7f947-174">Klikk på Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="7f947-174">Click Attach.</span></span>  
 23. <span data-ttu-id="7f947-175">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="7f947-175">Click New.</span></span>  
 24. <span data-ttu-id="7f947-176">Klikk på Fil.</span><span class="sxs-lookup"><span data-stu-id="7f947-176">Click File.</span></span>  
 25. <span data-ttu-id="7f947-177">Klikk på Bla gjennom og velg filen du lastet ned tidligere, Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="7f947-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="7f947-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f947-178">Close the page.</span></span>  
 27. <span data-ttu-id="7f947-179">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f947-179">Close the page.</span></span>  
 28. <span data-ttu-id="7f947-180">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f947-180">Close the page.</span></span>  
 29. <span data-ttu-id="7f947-181">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="7f947-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="7f947-182">Velg Ja i feltet Tillat oppretting av forhåndsmerknader for inaktive bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="7f947-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="7f947-183">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="7f947-183">Click Save.</span></span>  
 32. <span data-ttu-id="7f947-184">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f947-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
