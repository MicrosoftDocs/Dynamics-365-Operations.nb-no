---
title: Utforme ER-uttrykk for å kalle programklassemetoder
description: Denne veiledningen gir informasjon om hvordan du bruker den eksisterende programlogikken i elektronisk rapportering (ER)-konfigurasjoner på nytt ved å kalle nødvendige metoder for programklasser i ER-uttrykk.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdacd852eeed33b443a3c79b96fc4c4af04bb6b2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "357249"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a><span data-ttu-id="506bd-103">Utforme ER-uttrykk for å kalle programklassemetoder</span><span class="sxs-lookup"><span data-stu-id="506bd-103">Design ER expressions to call application class methods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="506bd-104">Denne veiledningen gir informasjon om hvordan du bruker den eksisterende programlogikken i elektronisk rapportering (ER)-konfigurasjoner på nytt ved å kalle nødvendige metoder for programklasser i ER-uttrykk.</span><span class="sxs-lookup"><span data-stu-id="506bd-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="506bd-105">Verdier for argumenter for kallklasser kan defineres dynamisk under kjøring: for eksempel basert på informasjon i analysedokumentet for å sikre nøyaktighet.</span><span class="sxs-lookup"><span data-stu-id="506bd-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="506bd-106">I denne veiledningen skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet, Litware, Inc. Denne fremgangsmåten er opprettet for brukere som har tilordnet rollen som Systemansvarlig eller Utvikler av elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="506bd-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="506bd-107">Disse trinnene kan fullføres ved hjelp av hvilket som helst datasett.</span><span class="sxs-lookup"><span data-stu-id="506bd-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="506bd-108">Du må også laste ned og lagre følgende fil lokalt: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="506bd-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="506bd-109">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "ER Opprette en konfigurasjonsleverandør og merke den som aktiv..</span><span class="sxs-lookup"><span data-stu-id="506bd-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="506bd-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="506bd-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="506bd-111">Kontroller at konfigurasjonsleverandøren for eksempelfirma Litware, Inc. er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="506bd-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="506bd-112">Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i prosedyren Opprette en konfigurasjonsleverandør og merke den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="506bd-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="506bd-113">La oss anta at du utformer en prosess for å analysere innkommende bankkontoutdrag for en oppdatering av programdata.</span><span class="sxs-lookup"><span data-stu-id="506bd-113">Let’s assume that you are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="506bd-114">Du vil motta innkommende bankkontoutdrag som TXT-filer som inneholder IBAN-koder.</span><span class="sxs-lookup"><span data-stu-id="506bd-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="506bd-115">Som en del av importprosessen for bankkontoutdrag må du validere riktigheten av disse IBAN-kodene ved hjelp av logikken som allerede finnes i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="506bd-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available in Dynamics 365 for Finance and Operations.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="506bd-116">Importere en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="506bd-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="506bd-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="506bd-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="506bd-118">Velg flisen Microsoft-leverandør.</span><span class="sxs-lookup"><span data-stu-id="506bd-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="506bd-119">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="506bd-119">Click Repositories.</span></span>
3. <span data-ttu-id="506bd-120">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="506bd-120">Click Show filters.</span></span>
4. <span data-ttu-id="506bd-121">Legg til et filterfelt 'Typenavn'.</span><span class="sxs-lookup"><span data-stu-id="506bd-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="506bd-122">I Navn-feltet angir du verdien “ressurser”, velger “inneholder”-filteroperatoren og klikker på Bruk.</span><span class="sxs-lookup"><span data-stu-id="506bd-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="506bd-123">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="506bd-123">Click Open.</span></span>
6. <span data-ttu-id="506bd-124">Velg Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="506bd-125">Hvis Importer-knappen på hurtigfanen Versjoner ikke er aktivert, har du allerede importert versjon 1 av ER-konfigurasjonen "Betalingsmodell".</span><span class="sxs-lookup"><span data-stu-id="506bd-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="506bd-126">Du kan hoppe over resten trinnene i denne underoppgaven.</span><span class="sxs-lookup"><span data-stu-id="506bd-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="506bd-127">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="506bd-127">Click Import.</span></span>
8. <span data-ttu-id="506bd-128">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="506bd-128">Click Yes.</span></span>
9. <span data-ttu-id="506bd-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="506bd-129">Close the page.</span></span>
10. <span data-ttu-id="506bd-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="506bd-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="506bd-131">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="506bd-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="506bd-132">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="506bd-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="506bd-133">Legg til et nytt ER-format for å analysere innkommende bankkontoutdrag i TXT-format.</span><span class="sxs-lookup"><span data-stu-id="506bd-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="506bd-134">Velg Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="506bd-135">Klikk Opprett konfigurasjon for å åpne dialogmenyen.</span><span class="sxs-lookup"><span data-stu-id="506bd-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="506bd-136">I feltet Ny angir du Format basert på datamodell PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="506bd-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="506bd-137">Skriv inn 'Importformat for bankkontoutdrag (eksempel)' i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="506bd-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="506bd-138">Importformat for bankkontoutdrag (eksempel)</span><span class="sxs-lookup"><span data-stu-id="506bd-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="506bd-139">Velg Ja i feltet Støtter dataimport.</span><span class="sxs-lookup"><span data-stu-id="506bd-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="506bd-140">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="506bd-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="506bd-141">Utforme ER-formatkonfigurasjonen – format</span><span class="sxs-lookup"><span data-stu-id="506bd-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="506bd-142">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="506bd-142">Click Designer.</span></span>
    * <span data-ttu-id="506bd-143">Det utformede formatet representerer den forventet strukturen for den eksterne filen i TXT-format.</span><span class="sxs-lookup"><span data-stu-id="506bd-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="506bd-144">Klikk Legg til rot for å åpne dialogmenyen.</span><span class="sxs-lookup"><span data-stu-id="506bd-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="506bd-145">Velg Tekst\Sekvens i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="506bd-146">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="506bd-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="506bd-147">Rot</span><span class="sxs-lookup"><span data-stu-id="506bd-147">Root</span></span>  
5. <span data-ttu-id="506bd-148">Velg Ny linje - Windows (CR LF) i Spesialtegn-feltet.</span><span class="sxs-lookup"><span data-stu-id="506bd-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="506bd-149">Alternativet Ny linje - Windows (CR LF) er valgt i Spesialtegn-feltet.</span><span class="sxs-lookup"><span data-stu-id="506bd-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="506bd-150">Basert på denne innstillingen, betraktes hver linje i analysefilen som en egen oppføring.</span><span class="sxs-lookup"><span data-stu-id="506bd-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="506bd-151">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="506bd-151">Click OK.</span></span>
7. <span data-ttu-id="506bd-152">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="506bd-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="506bd-153">Velg Tekst\Sekvens i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="506bd-154">I Navn-feltet skriver du inn Rader.</span><span class="sxs-lookup"><span data-stu-id="506bd-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="506bd-155">Rader</span><span class="sxs-lookup"><span data-stu-id="506bd-155">Rows</span></span>  
10. <span data-ttu-id="506bd-156">Velg "Én mange" i feltet Multiplisitet.</span><span class="sxs-lookup"><span data-stu-id="506bd-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="506bd-157">Alternativet Én mange er valgt i feltet Multiplisitet.</span><span class="sxs-lookup"><span data-stu-id="506bd-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="506bd-158">Basert på denne innstillingen, forventes det at minst én linje vises i analysefilen.</span><span class="sxs-lookup"><span data-stu-id="506bd-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="506bd-159">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="506bd-159">Click OK.</span></span>
12. <span data-ttu-id="506bd-160">Velg Rot\Rader i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="506bd-161">Klikk Legg sekvens.</span><span class="sxs-lookup"><span data-stu-id="506bd-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="506bd-162">I Navn-feltet skriver du inn Felt.</span><span class="sxs-lookup"><span data-stu-id="506bd-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="506bd-163">Felt</span><span class="sxs-lookup"><span data-stu-id="506bd-163">Fields</span></span>  
15. <span data-ttu-id="506bd-164">Velg "Nøyaktig én" i feltet Multiplisitet.</span><span class="sxs-lookup"><span data-stu-id="506bd-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="506bd-165">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="506bd-165">Click OK.</span></span>
17. <span data-ttu-id="506bd-166">I treet velger du Rot\Rader\Felt.</span><span class="sxs-lookup"><span data-stu-id="506bd-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="506bd-167">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="506bd-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="506bd-168">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="506bd-169">I Navn-feltet skriver du IBAN.</span><span class="sxs-lookup"><span data-stu-id="506bd-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="506bd-170">IBAN</span><span class="sxs-lookup"><span data-stu-id="506bd-170">IBAN</span></span>  
21. <span data-ttu-id="506bd-171">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="506bd-171">Click OK.</span></span>
    * <span data-ttu-id="506bd-172">Det er konfigurert at hver linje i analysefilen inneholder den eneste IBAN-koden.</span><span class="sxs-lookup"><span data-stu-id="506bd-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="506bd-173">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="506bd-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="506bd-174">Utforme ER-formatkonfigurasjonen – tilordne til datamodell</span><span class="sxs-lookup"><span data-stu-id="506bd-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="506bd-175">Klikk Tilordne format til modell.</span><span class="sxs-lookup"><span data-stu-id="506bd-175">Click Map format to model.</span></span>
2. <span data-ttu-id="506bd-176">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="506bd-176">Click New.</span></span>
3. <span data-ttu-id="506bd-177">I Definisjon-feltet skriver du inn BankToCustomerDebitCreditNotificationInitiation.</span><span class="sxs-lookup"><span data-stu-id="506bd-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="506bd-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="506bd-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="506bd-179">ResolveChanges definisjonen.</span><span class="sxs-lookup"><span data-stu-id="506bd-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="506bd-180">Skriv inn Tilordning til datamodell i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="506bd-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="506bd-181">Tilordning til datamodell</span><span class="sxs-lookup"><span data-stu-id="506bd-181">Mapping to data model</span></span>  
6. <span data-ttu-id="506bd-182">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="506bd-182">Click Save.</span></span>
7. <span data-ttu-id="506bd-183">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="506bd-183">Click Designer.</span></span>
8. <span data-ttu-id="506bd-184">Velg Dynamics 365 for Operations\Klasse i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="506bd-185">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="506bd-185">Click Add root.</span></span>
    * <span data-ttu-id="506bd-186">Legg til en ny datakilde for å kalle den eksisterende programlogikken for validering av IBAN-koder.</span><span class="sxs-lookup"><span data-stu-id="506bd-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="506bd-187">I Navn-feltet skriver du inn check_codes.</span><span class="sxs-lookup"><span data-stu-id="506bd-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="506bd-188">check_codes</span><span class="sxs-lookup"><span data-stu-id="506bd-188">check_codes</span></span>  
11. <span data-ttu-id="506bd-189">Skriv inn ISO7064 i feltet Klasse.</span><span class="sxs-lookup"><span data-stu-id="506bd-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="506bd-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="506bd-190">ISO7064</span></span>  
12. <span data-ttu-id="506bd-191">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="506bd-191">Click OK.</span></span>
13. <span data-ttu-id="506bd-192">Utvid 'format' i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="506bd-193">Utvid 'format\Rot: Sequence(Root) i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="506bd-194">I treet velger du "format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)'.</span><span class="sxs-lookup"><span data-stu-id="506bd-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="506bd-195">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="506bd-195">Click Bind.</span></span>
17. <span data-ttu-id="506bd-196">I treet utvider du "format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)'.</span><span class="sxs-lookup"><span data-stu-id="506bd-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="506bd-197">Utvid format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)" i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="506bd-198">Velg format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)\IBAN: String(IBAN) i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="506bd-199">Utvid Betalinger = format.Root.Rows i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="506bd-200">Utvid Betalinger = format.Root.Rows\Creditor Account(CreditorAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="506bd-201">Utvid Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identification i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="506bd-202">Velg Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="506bd-203">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="506bd-203">Click Bind.</span></span>
25. <span data-ttu-id="506bd-204">Klikk kategorien Valideringer.</span><span class="sxs-lookup"><span data-stu-id="506bd-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="506bd-205">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="506bd-205">Click New.</span></span>
    * <span data-ttu-id="506bd-206">Legg til en ny valideringsregel som viser en feil for alle linjer i analysefilen som inneholder ugyldig IBAN-kode.</span><span class="sxs-lookup"><span data-stu-id="506bd-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="506bd-207">Klikk Rediger betingelse.</span><span class="sxs-lookup"><span data-stu-id="506bd-207">Click Edit condition.</span></span>
28. <span data-ttu-id="506bd-208">Utvid check_codes i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="506bd-209">Velg check_codes\verifyMOD1271_36.</span><span class="sxs-lookup"><span data-stu-id="506bd-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="506bd-210">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="506bd-210">Click Add data source.</span></span>
31. <span data-ttu-id="506bd-211">I Formel-feltet skriver du inn 'check_codes.verifyMOD1271_36('.</span><span class="sxs-lookup"><span data-stu-id="506bd-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="506bd-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="506bd-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="506bd-213">Utvid 'format' i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="506bd-214">Utvid 'format\Rot: Sequence(Root) i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="506bd-215">I treet utvider du "format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)'.</span><span class="sxs-lookup"><span data-stu-id="506bd-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="506bd-216">Utvid format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)" i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="506bd-217">Velg format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)\IBAN: String(IBAN) i treet.</span><span class="sxs-lookup"><span data-stu-id="506bd-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="506bd-218">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="506bd-218">Click Add data source.</span></span>
38. <span data-ttu-id="506bd-219">I Formel-feltet skriver du inn 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="506bd-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="506bd-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="506bd-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="506bd-221">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="506bd-221">Click Save.</span></span>
40. <span data-ttu-id="506bd-222">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="506bd-222">Close the page.</span></span>
    * <span data-ttu-id="506bd-223">Valideringsbetingelsen er konfigurert til å returnere FALSE for en ugyldig IBAN-kode ved å kalle den eksisterende metoden 'verifyMOD1271_36' i programklassen 'ISO7064'.</span><span class="sxs-lookup"><span data-stu-id="506bd-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="506bd-224">Legg merke til at verdien til IBAN-koden defineres dynamisk under kjøring som argumentet for kallmetoden basert på innholdet i TXT-filen for analyse.</span><span class="sxs-lookup"><span data-stu-id="506bd-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="506bd-225">Klikk Rediger melding.</span><span class="sxs-lookup"><span data-stu-id="506bd-225">Click Edit message.</span></span>
42. <span data-ttu-id="506bd-226">Angi 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="506bd-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="506bd-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="506bd-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="506bd-228">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="506bd-228">Click Save.</span></span>
44. <span data-ttu-id="506bd-229">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="506bd-229">Close the page.</span></span>
45. <span data-ttu-id="506bd-230">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="506bd-230">Click Save.</span></span>
46. <span data-ttu-id="506bd-231">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="506bd-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="506bd-232">Kjøre formattilordningen</span><span class="sxs-lookup"><span data-stu-id="506bd-232">Run the format mapping</span></span>
<span data-ttu-id="506bd-233">For testformål kan du utføre formattilordningen med filen SampleIncomingMessage.txt som du lastet ned.</span><span class="sxs-lookup"><span data-stu-id="506bd-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="506bd-234">De genererte utdataene omfatter informasjon som importeres fra den valgte TXT-filen og fylles ut i den egendefinerte datamodellen under den reelle importen.</span><span class="sxs-lookup"><span data-stu-id="506bd-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="506bd-235">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="506bd-235">Click Run.</span></span>
    * <span data-ttu-id="506bd-236">Klikk Bla gjennom og gå til SampleIncomingMessage.txt-filen som du lastet ned tidligere.</span><span class="sxs-lookup"><span data-stu-id="506bd-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="506bd-237">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="506bd-237">Click OK.</span></span>
    * <span data-ttu-id="506bd-238">Gå gjennom utdataene i XML-format, som representerer dataene som er importert fra den valgte filen og overført til datamodellen.</span><span class="sxs-lookup"><span data-stu-id="506bd-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="506bd-239">Vær oppmerksom på at bare 3 linjer i den importerte TXT-filen ble behandlet.</span><span class="sxs-lookup"><span data-stu-id="506bd-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="506bd-240">IBAN-koden på linje 4 som ikke er gyldig, ble hoppet over, og en feilmelding gis i infologgen.</span><span class="sxs-lookup"><span data-stu-id="506bd-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  

