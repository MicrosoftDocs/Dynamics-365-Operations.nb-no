---
title: Utforme ER-uttrykk for å kalle programklassemetoder
description: Dette emnet beskriver hvordan du bruker den eksisterende programlogikken i konfigurasjoner for elektronisk rapportering på nytt ved å kalle opp nødvendige metoder for programklasser.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11b4d185703731d8491ad10bdeedea40ce811f5d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564100"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a><span data-ttu-id="88262-103">Utforme ER-uttrykk for å kalle programklassemetoder</span><span class="sxs-lookup"><span data-stu-id="88262-103">Design ER expressions to call application class methods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88262-104">Denne veiledningen gir informasjon om hvordan du bruker den eksisterende programlogikken i elektronisk rapportering (ER)-konfigurasjoner på nytt ved å kalle nødvendige metoder for programklasser i ER-uttrykk.</span><span class="sxs-lookup"><span data-stu-id="88262-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="88262-105">Verdier for argumenter for kallklasser kan defineres dynamisk under kjøring: for eksempel basert på informasjon i analysedokumentet for å sikre nøyaktighet.</span><span class="sxs-lookup"><span data-stu-id="88262-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="88262-106">I denne veiledningen skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet, Litware, Inc. Denne fremgangsmåten er opprettet for brukere som har tilordnet rollen som Systemansvarlig eller Utvikler av elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="88262-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="88262-107">Disse trinnene kan fullføres ved hjelp av hvilket som helst datasett.</span><span class="sxs-lookup"><span data-stu-id="88262-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="88262-108">Du må også laste ned og lagre følgende fil lokalt: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="88262-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="88262-109">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "ER Opprette en konfigurasjonsleverandør og merke den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="88262-109">To complete these steps, you must first complete the steps in the procedure, "ER Create a configuration provider and mark it as active."</span></span>

1. <span data-ttu-id="88262-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="88262-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="88262-111">Kontroller at konfigurasjonsleverandøren for eksempelfirma Litware, Inc. er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="88262-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="88262-112">Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="88262-112">If you don't see this configuration provider, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>   
    * <span data-ttu-id="88262-113">Du utformer en prosess for å analysere innkommende bankkontoutdrag for en oppdatering av programdata.</span><span class="sxs-lookup"><span data-stu-id="88262-113">You are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="88262-114">Du vil motta innkommende bankkontoutdrag som TXT-filer som inneholder IBAN-koder.</span><span class="sxs-lookup"><span data-stu-id="88262-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="88262-115">Som en del av importprosessen for bankkontoutdrag må du validere riktigheten av disse IBAN-kodene ved hjelp av logikken som allerede finnes.</span><span class="sxs-lookup"><span data-stu-id="88262-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="88262-116">Importere en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="88262-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="88262-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="88262-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="88262-118">Velg flisen Microsoft-leverandør.</span><span class="sxs-lookup"><span data-stu-id="88262-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="88262-119">Klikk på Repositorier.</span><span class="sxs-lookup"><span data-stu-id="88262-119">Click Repositories.</span></span>
3. <span data-ttu-id="88262-120">Klikk på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="88262-120">Click Show filters.</span></span>
4. <span data-ttu-id="88262-121">Legg til et "Typenavn"-filterfelt.</span><span class="sxs-lookup"><span data-stu-id="88262-121">Add a filter field 'Type name'.</span></span> <span data-ttu-id="88262-122">I Navn-feltet angir du verdien "ressurser", velger "inneholder"-filteroperatoren og klikker på Bruk.</span><span class="sxs-lookup"><span data-stu-id="88262-122">In the Name field, enter the value "resources", select the "contains" filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="88262-123">Klikk på Åpne.</span><span class="sxs-lookup"><span data-stu-id="88262-123">Click Open.</span></span>
6. <span data-ttu-id="88262-124">Velg Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="88262-125">Hvis Importer-knappen på hurtigfanen Versjoner ikke er aktivert, har du allerede importert versjon 1 av ER-konfigurasjonen "Betalingsmodell".</span><span class="sxs-lookup"><span data-stu-id="88262-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration 'Payment model'.</span></span> <span data-ttu-id="88262-126">Du kan hoppe over resten trinnene i denne underoppgaven.</span><span class="sxs-lookup"><span data-stu-id="88262-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="88262-127">Klikk på Importer.</span><span class="sxs-lookup"><span data-stu-id="88262-127">Click Import.</span></span>
8. <span data-ttu-id="88262-128">Klikk på Ja.</span><span class="sxs-lookup"><span data-stu-id="88262-128">Click Yes.</span></span>
9. <span data-ttu-id="88262-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="88262-129">Close the page.</span></span>
10. <span data-ttu-id="88262-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="88262-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="88262-131">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="88262-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="88262-132">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="88262-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="88262-133">Legg til et nytt ER-format for å analysere innkommende bankkontoutdrag i TXT-format.</span><span class="sxs-lookup"><span data-stu-id="88262-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="88262-134">Velg Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="88262-135">Klikk på Opprett konfigurasjon for å åpne dialogmenyen.</span><span class="sxs-lookup"><span data-stu-id="88262-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="88262-136">I feltet Ny angir du Format basert på datamodell PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="88262-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="88262-137">Skriv inn 'Importformat for bankkontoutdrag (eksempel)' i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="88262-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="88262-138">Importformat for bankkontoutdrag (eksempel)</span><span class="sxs-lookup"><span data-stu-id="88262-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="88262-139">Velg Ja i feltet Støtter dataimport.</span><span class="sxs-lookup"><span data-stu-id="88262-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="88262-140">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="88262-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="88262-141">Utforme ER-formatkonfigurasjonen – format</span><span class="sxs-lookup"><span data-stu-id="88262-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="88262-142">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="88262-142">Click Designer.</span></span>
    * <span data-ttu-id="88262-143">Det utformede formatet representerer den forventet strukturen for den eksterne filen i TXT-format.</span><span class="sxs-lookup"><span data-stu-id="88262-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="88262-144">Klikk på Legg til rot for å åpne dialogmenyen.</span><span class="sxs-lookup"><span data-stu-id="88262-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="88262-145">Velg Tekst\Sekvens i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="88262-146">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="88262-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="88262-147">Rot</span><span class="sxs-lookup"><span data-stu-id="88262-147">Root</span></span>  
5. <span data-ttu-id="88262-148">Velg Ny linje - Windows (CR LF) i Spesialtegn-feltet.</span><span class="sxs-lookup"><span data-stu-id="88262-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="88262-149">Alternativet Ny linje - Windows (CR LF) er valgt i Spesialtegn-feltet.</span><span class="sxs-lookup"><span data-stu-id="88262-149">The option 'New line - Windows (CR LF)' has been selected in the 'Special characters' field.</span></span> <span data-ttu-id="88262-150">Basert på denne innstillingen, betraktes hver linje i analysefilen som en egen oppføring.</span><span class="sxs-lookup"><span data-stu-id="88262-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="88262-151">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="88262-151">Click OK.</span></span>
7. <span data-ttu-id="88262-152">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="88262-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="88262-153">Velg Tekst\Sekvens i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="88262-154">I Navn-feltet skriver du inn Rader.</span><span class="sxs-lookup"><span data-stu-id="88262-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="88262-155">Rader</span><span class="sxs-lookup"><span data-stu-id="88262-155">Rows</span></span>  
10. <span data-ttu-id="88262-156">Velg "Én mange" i feltet Multiplisitet.</span><span class="sxs-lookup"><span data-stu-id="88262-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="88262-157">Alternativet Én mange er valgt i feltet Multiplisitet.</span><span class="sxs-lookup"><span data-stu-id="88262-157">The option 'One many' has been selected in the 'Multiplicity' field.</span></span> <span data-ttu-id="88262-158">Basert på denne innstillingen, forventes det at minst én linje vises i analysefilen.</span><span class="sxs-lookup"><span data-stu-id="88262-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="88262-159">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="88262-159">Click OK.</span></span>
12. <span data-ttu-id="88262-160">Velg Rot\Rader i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="88262-161">Klikk på Legg sekvens.</span><span class="sxs-lookup"><span data-stu-id="88262-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="88262-162">I Navn-feltet skriver du inn Felt.</span><span class="sxs-lookup"><span data-stu-id="88262-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="88262-163">Felt</span><span class="sxs-lookup"><span data-stu-id="88262-163">Fields</span></span>  
15. <span data-ttu-id="88262-164">Velg "Nøyaktig én" i feltet Multiplisitet.</span><span class="sxs-lookup"><span data-stu-id="88262-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="88262-165">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="88262-165">Click OK.</span></span>
17. <span data-ttu-id="88262-166">I treet velger du Rot\Rader\Felt.</span><span class="sxs-lookup"><span data-stu-id="88262-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="88262-167">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="88262-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="88262-168">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="88262-169">I Navn-feltet skriver du IBAN.</span><span class="sxs-lookup"><span data-stu-id="88262-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="88262-170">IBAN</span><span class="sxs-lookup"><span data-stu-id="88262-170">IBAN</span></span>  
21. <span data-ttu-id="88262-171">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="88262-171">Click OK.</span></span>
    * <span data-ttu-id="88262-172">Det er konfigurert at hver linje i analysefilen inneholder den eneste IBAN-koden.</span><span class="sxs-lookup"><span data-stu-id="88262-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="88262-173">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="88262-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="88262-174">Utforme ER-formatkonfigurasjonen – tilordne til datamodell</span><span class="sxs-lookup"><span data-stu-id="88262-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="88262-175">Klikk på Tilordne format til modell.</span><span class="sxs-lookup"><span data-stu-id="88262-175">Click Map format to model.</span></span>
2. <span data-ttu-id="88262-176">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="88262-176">Click New.</span></span>
3. <span data-ttu-id="88262-177">I Definisjon-feltet skriver du inn BankToCustomerDebitCreditNotificationInitiation.</span><span class="sxs-lookup"><span data-stu-id="88262-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="88262-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="88262-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="88262-179">ResolveChanges definisjonen.</span><span class="sxs-lookup"><span data-stu-id="88262-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="88262-180">Skriv inn Tilordning til datamodell i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="88262-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="88262-181">Tilordning til datamodell</span><span class="sxs-lookup"><span data-stu-id="88262-181">Mapping to data model</span></span>  
6. <span data-ttu-id="88262-182">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="88262-182">Click Save.</span></span>
7. <span data-ttu-id="88262-183">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="88262-183">Click Designer.</span></span>
8. <span data-ttu-id="88262-184">Velg Dynamics 365 for Operations\Klasse i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="88262-185">Klikk på Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="88262-185">Click Add root.</span></span>
    * <span data-ttu-id="88262-186">Legg til en ny datakilde for å kalle den eksisterende programlogikken for validering av IBAN-koder.</span><span class="sxs-lookup"><span data-stu-id="88262-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="88262-187">I Navn-feltet skriver du inn check_codes.</span><span class="sxs-lookup"><span data-stu-id="88262-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="88262-188">check_codes</span><span class="sxs-lookup"><span data-stu-id="88262-188">check_codes</span></span>  
11. <span data-ttu-id="88262-189">Skriv inn ISO7064 i feltet Klasse.</span><span class="sxs-lookup"><span data-stu-id="88262-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="88262-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="88262-190">ISO7064</span></span>  
12. <span data-ttu-id="88262-191">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="88262-191">Click OK.</span></span>
13. <span data-ttu-id="88262-192">Utvid 'format' i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="88262-193">Utvid 'format\Rot: Sequence(Root) i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="88262-194">I treet velger du "format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)'.</span><span class="sxs-lookup"><span data-stu-id="88262-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="88262-195">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="88262-195">Click Bind.</span></span>
17. <span data-ttu-id="88262-196">I treet utvider du "format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)'.</span><span class="sxs-lookup"><span data-stu-id="88262-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="88262-197">Utvid format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)" i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="88262-198">Velg format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)\IBAN: String(IBAN) i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="88262-199">Utvid Betalinger = format.Root.Rows i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="88262-200">Utvid Betalinger = format.Root.Rows\Creditor Account(CreditorAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="88262-201">Utvid Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identification i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="88262-202">Velg Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="88262-203">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="88262-203">Click Bind.</span></span>
25. <span data-ttu-id="88262-204">Klikk på fanen Valideringer.</span><span class="sxs-lookup"><span data-stu-id="88262-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="88262-205">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="88262-205">Click New.</span></span>
    * <span data-ttu-id="88262-206">Legg til en ny valideringsregel som viser en feil for alle linjer i analysefilen som inneholder ugyldig IBAN-kode.</span><span class="sxs-lookup"><span data-stu-id="88262-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="88262-207">Klikk på Rediger betingelse.</span><span class="sxs-lookup"><span data-stu-id="88262-207">Click Edit condition.</span></span>
28. <span data-ttu-id="88262-208">Utvid check_codes i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="88262-209">Velg check_codes\verifyMOD1271_36.</span><span class="sxs-lookup"><span data-stu-id="88262-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="88262-210">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="88262-210">Click Add data source.</span></span>
31. <span data-ttu-id="88262-211">I Formel-feltet skriver du inn 'check_codes.verifyMOD1271_36('.</span><span class="sxs-lookup"><span data-stu-id="88262-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="88262-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="88262-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="88262-213">Utvid 'format' i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="88262-214">Utvid 'format\Rot: Sequence(Root) i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="88262-215">I treet utvider du "format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)'.</span><span class="sxs-lookup"><span data-stu-id="88262-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="88262-216">Utvid format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)" i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="88262-217">Velg format\Rot: Sequence(Root)\Rader: Sekvens 1..\* (Rader)\Felt: Sekvens 1..1 (Felt)\IBAN: String(IBAN) i treet.</span><span class="sxs-lookup"><span data-stu-id="88262-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="88262-218">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="88262-218">Click Add data source.</span></span>
38. <span data-ttu-id="88262-219">I Formel-feltet skriver du inn 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="88262-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="88262-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="88262-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="88262-221">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="88262-221">Click Save.</span></span>
40. <span data-ttu-id="88262-222">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="88262-222">Close the page.</span></span>
    * <span data-ttu-id="88262-223">Valideringsbetingelsen er konfigurert til å returnere FALSE for en ugyldig IBAN-kode ved å kalle den eksisterende metoden "verifyMOD1271_36" i programklassen "ISO7064".</span><span class="sxs-lookup"><span data-stu-id="88262-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method 'verifyMOD1271_36' of the application class 'ISO7064'.</span></span> <span data-ttu-id="88262-224">Legg merke til at verdien til IBAN-koden defineres dynamisk under kjøring som argumentet for kallmetoden basert på innholdet i TXT-filen for analyse.</span><span class="sxs-lookup"><span data-stu-id="88262-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="88262-225">Klikk på Rediger melding.</span><span class="sxs-lookup"><span data-stu-id="88262-225">Click Edit message.</span></span>
42. <span data-ttu-id="88262-226">Angi 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="88262-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="88262-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="88262-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="88262-228">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="88262-228">Click Save.</span></span>
44. <span data-ttu-id="88262-229">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="88262-229">Close the page.</span></span>
45. <span data-ttu-id="88262-230">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="88262-230">Click Save.</span></span>
46. <span data-ttu-id="88262-231">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="88262-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="88262-232">Kjøre formattilordningen</span><span class="sxs-lookup"><span data-stu-id="88262-232">Run the format mapping</span></span>
<span data-ttu-id="88262-233">For testformål kan du utføre formattilordningen med filen SampleIncomingMessage.txt som du lastet ned.</span><span class="sxs-lookup"><span data-stu-id="88262-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="88262-234">De genererte utdataene omfatter informasjon som importeres fra den valgte TXT-filen og fylles ut i den egendefinerte datamodellen under den reelle importen.</span><span class="sxs-lookup"><span data-stu-id="88262-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="88262-235">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="88262-235">Click Run.</span></span>
    * <span data-ttu-id="88262-236">Klikk på Bla gjennom og gå til SampleIncomingMessage.txt-filen som du lastet ned tidligere.</span><span class="sxs-lookup"><span data-stu-id="88262-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="88262-237">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="88262-237">Click OK.</span></span>
    * <span data-ttu-id="88262-238">Gå gjennom utdataene i XML-format, som representerer dataene som er importert fra den valgte filen og overført til datamodellen.</span><span class="sxs-lookup"><span data-stu-id="88262-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="88262-239">Vær oppmerksom på at bare 3 linjer i den importerte TXT-filen ble behandlet.</span><span class="sxs-lookup"><span data-stu-id="88262-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="88262-240">IBAN-koden på linje 4 som ikke er gyldig, ble hoppet over, og en feilmelding gis i infologgen.</span><span class="sxs-lookup"><span data-stu-id="88262-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]