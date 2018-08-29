--- 
title: "Utforme ER-uttrykk for å kalle programklassemetoder"
description: "Denne veiledningen gir informasjon om hvordan du bruker den eksisterende programlogikken i elektronisk rapportering (ER)-konfigurasjoner på nytt ved å kalle nødvendige metoder for programklasser i ER-uttrykk."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fdacd852eeed33b443a3c79b96fc4c4af04bb6b2
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-expressions-to-call-application-class-methods"></a><span data-ttu-id="80a9f-103">Utforme ER-uttrykk for å kalle programklassemetoder</span><span class="sxs-lookup"><span data-stu-id="80a9f-103">Design ER expressions to call application class methods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="80a9f-104">Denne veiledningen gir informasjon om hvordan du bruker den eksisterende programlogikken i elektronisk rapportering (ER)-konfigurasjoner på nytt ved å kalle nødvendige metoder for programklasser i ER-uttrykk.</span><span class="sxs-lookup"><span data-stu-id="80a9f-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="80a9f-105">Verdier for argumenter for kallklasser kan defineres dynamisk under kjøring: for eksempel basert på informasjon i analysedokumentet for å sikre nøyaktighet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="80a9f-106">I denne veiledningen skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet, Litware, Inc. Denne fremgangsmåten er opprettet for brukere som har tilordnet rollen som Systemansvarlig eller Utvikler av elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="80a9f-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="80a9f-107">Disse trinnene kan fullføres ved hjelp av hvilket som helst datasett.</span><span class="sxs-lookup"><span data-stu-id="80a9f-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="80a9f-108">Du må også laste ned og lagre følgende fil lokalt: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="80a9f-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="80a9f-109">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "ER Opprette en konfigurasjonsleverandør og merke den som aktiv..</span><span class="sxs-lookup"><span data-stu-id="80a9f-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="80a9f-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="80a9f-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="80a9f-111">Kontroller at konfigurasjonsleverandøren for eksempelfirma Litware, Inc. er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="80a9f-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="80a9f-112">Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i prosedyren Opprette en konfigurasjonsleverandør og merke den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="80a9f-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="80a9f-113">La oss anta at du utformer en prosess for å analysere innkommende bankkontoutdrag for en oppdatering av programdata.</span><span class="sxs-lookup"><span data-stu-id="80a9f-113">Let’s assume that you are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="80a9f-114">Du vil motta innkommende bankkontoutdrag som TXT-filer som inneholder IBAN-koder.</span><span class="sxs-lookup"><span data-stu-id="80a9f-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="80a9f-115">Som en del av importprosessen for bankkontoutdrag må du validere riktigheten av disse IBAN-kodene ved hjelp av logikken som allerede finnes i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80a9f-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available in Dynamics 365 for Finance and Operations.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="80a9f-116">Importere en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="80a9f-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="80a9f-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="80a9f-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="80a9f-118">Velg flisen Microsoft-leverandør.</span><span class="sxs-lookup"><span data-stu-id="80a9f-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="80a9f-119">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="80a9f-119">Click Repositories.</span></span>
3. <span data-ttu-id="80a9f-120">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="80a9f-120">Click Show filters.</span></span>
4. <span data-ttu-id="80a9f-121">Legg til et filterfelt 'Typenavn'.</span><span class="sxs-lookup"><span data-stu-id="80a9f-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="80a9f-122">I Navn-feltet angir du verdien “ressurser”, velger “inneholder”-filteroperatoren og klikker på Bruk.</span><span class="sxs-lookup"><span data-stu-id="80a9f-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="80a9f-123">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="80a9f-123">Click Open.</span></span>
6. <span data-ttu-id="80a9f-124">Velg Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="80a9f-125">Hvis Importer-knappen på hurtigfanen Versjoner ikke er aktivert, har du allerede importert versjon 1 av ER-konfigurasjonen "Betalingsmodell".</span><span class="sxs-lookup"><span data-stu-id="80a9f-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="80a9f-126">Du kan hoppe over resten trinnene i denne underoppgaven.</span><span class="sxs-lookup"><span data-stu-id="80a9f-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="80a9f-127">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="80a9f-127">Click Import.</span></span>
8. <span data-ttu-id="80a9f-128">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="80a9f-128">Click Yes.</span></span>
9. <span data-ttu-id="80a9f-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="80a9f-129">Close the page.</span></span>
10. <span data-ttu-id="80a9f-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="80a9f-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="80a9f-131">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="80a9f-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="80a9f-132">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="80a9f-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="80a9f-133">Legg til et nytt ER-format for å analysere innkommende bankkontoutdrag i TXT-format.</span><span class="sxs-lookup"><span data-stu-id="80a9f-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="80a9f-134">Velg Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="80a9f-135">Klikk Opprett konfigurasjon for å åpne dialogmenyen.</span><span class="sxs-lookup"><span data-stu-id="80a9f-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="80a9f-136">I feltet Ny angir du Format basert på datamodell PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="80a9f-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="80a9f-137">Skriv inn 'Importformat for bankkontoutdrag (eksempel)' i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="80a9f-138">Importformat for bankkontoutdrag (eksempel)</span><span class="sxs-lookup"><span data-stu-id="80a9f-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="80a9f-139">Velg Ja i feltet Støtter dataimport.</span><span class="sxs-lookup"><span data-stu-id="80a9f-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="80a9f-140">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="80a9f-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="80a9f-141">Utforme ER-formatkonfigurasjonen – format</span><span class="sxs-lookup"><span data-stu-id="80a9f-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="80a9f-142">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="80a9f-142">Click Designer.</span></span>
    * <span data-ttu-id="80a9f-143">Det utformede formatet representerer den forventet strukturen for den eksterne filen i TXT-format.</span><span class="sxs-lookup"><span data-stu-id="80a9f-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="80a9f-144">Klikk Legg til rot for å åpne dialogmenyen.</span><span class="sxs-lookup"><span data-stu-id="80a9f-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="80a9f-145">Velg Tekst\Sekvens i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="80a9f-146">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="80a9f-147">Rot</span><span class="sxs-lookup"><span data-stu-id="80a9f-147">Root</span></span>  
5. <span data-ttu-id="80a9f-148">Velg Ny linje - Windows (CR LF) i Spesialtegn-feltet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="80a9f-149">Alternativet Ny linje - Windows (CR LF) er valgt i Spesialtegn-feltet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="80a9f-150">Basert på denne innstillingen, betraktes hver linje i analysefilen som en egen oppføring.</span><span class="sxs-lookup"><span data-stu-id="80a9f-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="80a9f-151">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="80a9f-151">Click OK.</span></span>
7. <span data-ttu-id="80a9f-152">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="80a9f-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="80a9f-153">Velg Tekst\Sekvens i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="80a9f-154">I Navn-feltet skriver du inn Rader.</span><span class="sxs-lookup"><span data-stu-id="80a9f-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="80a9f-155">Rader</span><span class="sxs-lookup"><span data-stu-id="80a9f-155">Rows</span></span>  
10. <span data-ttu-id="80a9f-156">Velg "Én mange" i feltet Multiplisitet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="80a9f-157">Alternativet Én mange er valgt i feltet Multiplisitet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="80a9f-158">Basert på denne innstillingen, forventes det at minst én linje vises i analysefilen.</span><span class="sxs-lookup"><span data-stu-id="80a9f-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="80a9f-159">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="80a9f-159">Click OK.</span></span>
12. <span data-ttu-id="80a9f-160">Velg Rot\Rader i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="80a9f-161">Klikk Legg sekvens.</span><span class="sxs-lookup"><span data-stu-id="80a9f-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="80a9f-162">I Navn-feltet skriver du inn Felt.</span><span class="sxs-lookup"><span data-stu-id="80a9f-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="80a9f-163">Felt</span><span class="sxs-lookup"><span data-stu-id="80a9f-163">Fields</span></span>  
15. <span data-ttu-id="80a9f-164">Velg "Nøyaktig én" i feltet Multiplisitet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="80a9f-165">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="80a9f-165">Click OK.</span></span>
17. <span data-ttu-id="80a9f-166">I treet velger du Rot\Rader\Felt.</span><span class="sxs-lookup"><span data-stu-id="80a9f-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="80a9f-167">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="80a9f-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="80a9f-168">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="80a9f-169">I Navn-feltet skriver du IBAN.</span><span class="sxs-lookup"><span data-stu-id="80a9f-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="80a9f-170">IBAN</span><span class="sxs-lookup"><span data-stu-id="80a9f-170">IBAN</span></span>  
21. <span data-ttu-id="80a9f-171">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="80a9f-171">Click OK.</span></span>
    * <span data-ttu-id="80a9f-172">Det er konfigurert at hver linje i analysefilen inneholder den eneste IBAN-koden.</span><span class="sxs-lookup"><span data-stu-id="80a9f-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="80a9f-173">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="80a9f-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="80a9f-174">Utforme ER-formatkonfigurasjonen – tilordne til datamodell</span><span class="sxs-lookup"><span data-stu-id="80a9f-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="80a9f-175">Klikk Tilordne format til modell.</span><span class="sxs-lookup"><span data-stu-id="80a9f-175">Click Map format to model.</span></span>
2. <span data-ttu-id="80a9f-176">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="80a9f-176">Click New.</span></span>
3. <span data-ttu-id="80a9f-177">I Definisjon-feltet skriver du inn BankToCustomerDebitCreditNotificationInitiation.</span><span class="sxs-lookup"><span data-stu-id="80a9f-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="80a9f-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="80a9f-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="80a9f-179">ResolveChanges definisjonen.</span><span class="sxs-lookup"><span data-stu-id="80a9f-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="80a9f-180">Skriv inn Tilordning til datamodell i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="80a9f-181">Tilordning til datamodell</span><span class="sxs-lookup"><span data-stu-id="80a9f-181">Mapping to data model</span></span>  
6. <span data-ttu-id="80a9f-182">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="80a9f-182">Click Save.</span></span>
7. <span data-ttu-id="80a9f-183">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="80a9f-183">Click Designer.</span></span>
8. <span data-ttu-id="80a9f-184">I treet velger du Dynamics 365 for Operations\Klasse.</span><span class="sxs-lookup"><span data-stu-id="80a9f-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="80a9f-185">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="80a9f-185">Click Add root.</span></span>
    * <span data-ttu-id="80a9f-186">Legg til en ny datakilde for å kalle den eksisterende programlogikken for validering av IBAN-koder.</span><span class="sxs-lookup"><span data-stu-id="80a9f-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="80a9f-187">I Navn-feltet skriver du inn check_codes.</span><span class="sxs-lookup"><span data-stu-id="80a9f-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="80a9f-188">check_codes</span><span class="sxs-lookup"><span data-stu-id="80a9f-188">check_codes</span></span>  
11. <span data-ttu-id="80a9f-189">Skriv inn ISO7064 i feltet Klasse.</span><span class="sxs-lookup"><span data-stu-id="80a9f-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="80a9f-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="80a9f-190">ISO7064</span></span>  
12. <span data-ttu-id="80a9f-191">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="80a9f-191">Click OK.</span></span>
13. <span data-ttu-id="80a9f-192">Utvid 'format' i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="80a9f-193">Utvid 'format\Rot: Sequence(Root) i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="80a9f-194">I treet velger du "format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)'.</span><span class="sxs-lookup"><span data-stu-id="80a9f-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="80a9f-195">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="80a9f-195">Click Bind.</span></span>
17. <span data-ttu-id="80a9f-196">I treet utvider du "format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)'.</span><span class="sxs-lookup"><span data-stu-id="80a9f-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="80a9f-197">Utvid format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)" i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="80a9f-198">Velg format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)\IBAN: String(IBAN) i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="80a9f-199">Utvid Betalinger = format.Root.Rows i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="80a9f-200">Utvid Betalinger = format.Root.Rows\Creditor Account(CreditorAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="80a9f-201">Utvid Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identification i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="80a9f-202">Velg Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="80a9f-203">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="80a9f-203">Click Bind.</span></span>
25. <span data-ttu-id="80a9f-204">Klikk kategorien Valideringer.</span><span class="sxs-lookup"><span data-stu-id="80a9f-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="80a9f-205">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="80a9f-205">Click New.</span></span>
    * <span data-ttu-id="80a9f-206">Legg til en ny valideringsregel som viser en feil for alle linjer i analysefilen som inneholder ugyldig IBAN-kode.</span><span class="sxs-lookup"><span data-stu-id="80a9f-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="80a9f-207">Klikk Rediger betingelse.</span><span class="sxs-lookup"><span data-stu-id="80a9f-207">Click Edit condition.</span></span>
28. <span data-ttu-id="80a9f-208">Utvid check_codes i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="80a9f-209">Velg check_codes\verifyMOD1271_36.</span><span class="sxs-lookup"><span data-stu-id="80a9f-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="80a9f-210">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="80a9f-210">Click Add data source.</span></span>
31. <span data-ttu-id="80a9f-211">I Formel-feltet skriver du inn 'check_codes.verifyMOD1271_36('.</span><span class="sxs-lookup"><span data-stu-id="80a9f-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="80a9f-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="80a9f-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="80a9f-213">Utvid 'format' i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="80a9f-214">Utvid 'format\Rot: Sequence(Root) i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="80a9f-215">I treet utvider du "format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)'.</span><span class="sxs-lookup"><span data-stu-id="80a9f-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="80a9f-216">Utvid format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)" i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="80a9f-217">Velg format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)\IBAN: String(IBAN) i treet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="80a9f-218">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="80a9f-218">Click Add data source.</span></span>
38. <span data-ttu-id="80a9f-219">I Formel-feltet skriver du inn 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="80a9f-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="80a9f-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="80a9f-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="80a9f-221">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="80a9f-221">Click Save.</span></span>
40. <span data-ttu-id="80a9f-222">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="80a9f-222">Close the page.</span></span>
    * <span data-ttu-id="80a9f-223">Valideringsbetingelsen er konfigurert til å returnere FALSE for en ugyldig IBAN-kode ved å kalle den eksisterende metoden 'verifyMOD1271_36' i programklassen 'ISO7064'.</span><span class="sxs-lookup"><span data-stu-id="80a9f-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="80a9f-224">Legg merke til at verdien til IBAN-koden defineres dynamisk under kjøring som argumentet for kallmetoden basert på innholdet i TXT-filen for analyse.</span><span class="sxs-lookup"><span data-stu-id="80a9f-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="80a9f-225">Klikk Rediger melding.</span><span class="sxs-lookup"><span data-stu-id="80a9f-225">Click Edit message.</span></span>
42. <span data-ttu-id="80a9f-226">Angi 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="80a9f-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="80a9f-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="80a9f-228">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="80a9f-228">Click Save.</span></span>
44. <span data-ttu-id="80a9f-229">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="80a9f-229">Close the page.</span></span>
45. <span data-ttu-id="80a9f-230">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="80a9f-230">Click Save.</span></span>
46. <span data-ttu-id="80a9f-231">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="80a9f-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="80a9f-232">Kjøre formattilordningen</span><span class="sxs-lookup"><span data-stu-id="80a9f-232">Run the format mapping</span></span>
<span data-ttu-id="80a9f-233">For testformål kan du utføre formattilordningen med filen SampleIncomingMessage.txt som du lastet ned.</span><span class="sxs-lookup"><span data-stu-id="80a9f-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="80a9f-234">De genererte utdataene omfatter informasjon som importeres fra den valgte TXT-filen og fylles ut i den egendefinerte datamodellen under den reelle importen.</span><span class="sxs-lookup"><span data-stu-id="80a9f-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="80a9f-235">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="80a9f-235">Click Run.</span></span>
    * <span data-ttu-id="80a9f-236">Klikk Bla gjennom og gå til SampleIncomingMessage.txt-filen som du lastet ned tidligere.</span><span class="sxs-lookup"><span data-stu-id="80a9f-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="80a9f-237">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="80a9f-237">Click OK.</span></span>
    * <span data-ttu-id="80a9f-238">Gå gjennom utdataene i XML-format, som representerer dataene som er importert fra den valgte filen og overført til datamodellen.</span><span class="sxs-lookup"><span data-stu-id="80a9f-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="80a9f-239">Vær oppmerksom på at bare 3 linjer i den importerte TXT-filen ble behandlet.</span><span class="sxs-lookup"><span data-stu-id="80a9f-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="80a9f-240">IBAN-koden på linje 4 som ikke er gyldig, ble hoppet over, og en feilmelding gis i infologgen.</span><span class="sxs-lookup"><span data-stu-id="80a9f-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  


