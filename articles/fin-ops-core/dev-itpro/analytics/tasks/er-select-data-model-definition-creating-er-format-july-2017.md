---
title: Velge datamodelldefinisjoner når du oppretter formater
description: For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren "ER Opprette en konfigurasjonsleverandør og merke den som aktiv".
author: NickSelin
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
ms.openlocfilehash: b01f7afb6ca3bd1f317c25202e0cf72231008fca
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744969"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="3bf26-103">Velge datamodelldefinisjoner når du oppretter formater</span><span class="sxs-lookup"><span data-stu-id="3bf26-103">Select data model definitions when you create formats</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3bf26-104">For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren "ER Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="3bf26-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="3bf26-105">Denne fremgangsmåten viser hvordan en modell rotelementet kan velges som en modell for datadefinisjon for å sette inn en elektronisk rapportering (ER)-formatkonfigurasjonen som er utformet for å generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3bf26-105">This procedure shows how a model's root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="3bf26-106">I denne prosedyren skal du legge til en ny ER-formatkonfigurasjon for eksempelfirmaet "Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="3bf26-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="3bf26-107">Denne fremgangsmåten er ment for brukere som har den systemansvarlige eller elektronisk rapportering utvikler-rolle tilordnet.</span><span class="sxs-lookup"><span data-stu-id="3bf26-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="3bf26-108">Trinnene kan fullføres ved hjelp av ethvert datasett.</span><span class="sxs-lookup"><span data-stu-id="3bf26-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="3bf26-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="3bf26-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="3bf26-110">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="3bf26-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="3bf26-111">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="3bf26-111">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="3bf26-112">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3bf26-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="3bf26-113">Legg til en ny ER-datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3bf26-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="3bf26-114">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="3bf26-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="3bf26-115">Vi legger til en ny ER-modellkonfigurasjon som inneholder en datamodell som skal brukes som datakilde for generering av ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="3bf26-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="3bf26-116">I Navn-feltet skriver du inn "Betalingingsmodell (fiktiv)".</span><span class="sxs-lookup"><span data-stu-id="3bf26-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="3bf26-117">Betalingsmodell (fiktiv)</span><span class="sxs-lookup"><span data-stu-id="3bf26-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="3bf26-118">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3bf26-118">Click Create configuration.</span></span>
4. <span data-ttu-id="3bf26-119">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="3bf26-119">Click Designer.</span></span>
    * <span data-ttu-id="3bf26-120">Åpne ER-utforming for å angi strukturen for datamodellen av denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="3bf26-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="3bf26-121">Anta at vi utformer datamodellen for betalinger virksomheten domene til å støtte 2 betalingsmåter – Overfør kreditt og AvtaleGiro som.</span><span class="sxs-lookup"><span data-stu-id="3bf26-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="3bf26-122">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="3bf26-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="3bf26-123">I Navn-feltet skriver du inn "Betalinger – Overfør kreditt".</span><span class="sxs-lookup"><span data-stu-id="3bf26-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="3bf26-124">Betalinger – Overfør kreditt</span><span class="sxs-lookup"><span data-stu-id="3bf26-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="3bf26-125">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="3bf26-125">Click Add.</span></span>
8. <span data-ttu-id="3bf26-126">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="3bf26-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="3bf26-127">I feltet Ny node som en for angir du Modellrot.</span><span class="sxs-lookup"><span data-stu-id="3bf26-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="3bf26-128">I Navn-feltet skriver du inn "Betalinger – avtalegiro".</span><span class="sxs-lookup"><span data-stu-id="3bf26-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="3bf26-129">Betalinger – direktedebet</span><span class="sxs-lookup"><span data-stu-id="3bf26-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="3bf26-130">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="3bf26-130">Click Add.</span></span>
12. <span data-ttu-id="3bf26-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3bf26-131">Click Save.</span></span>
13. <span data-ttu-id="3bf26-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3bf26-132">Close the page.</span></span>
14. <span data-ttu-id="3bf26-133">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="3bf26-133">Click Change status.</span></span>
    * <span data-ttu-id="3bf26-134">Fullfør utkastversjonen av modellen for å gjøre den tilgjengelig i nye modellen tilordningene og formater.</span><span class="sxs-lookup"><span data-stu-id="3bf26-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="3bf26-135">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="3bf26-135">Click Complete.</span></span>
16. <span data-ttu-id="3bf26-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3bf26-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="3bf26-137">Start for å angi en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3bf26-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="3bf26-138">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="3bf26-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="3bf26-139">I feltet Ny angir du Format basert på datamodellen Betalingsmodell (fiktiv).</span><span class="sxs-lookup"><span data-stu-id="3bf26-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="3bf26-140">Angi eller velg en verdi i feltet Definisjon av datamodell.</span><span class="sxs-lookup"><span data-stu-id="3bf26-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="3bf26-141">Legg merke til at alle varer i roten av valgte datamodellen som er tilgjengelige som en modell datadefinisjon.</span><span class="sxs-lookup"><span data-stu-id="3bf26-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="3bf26-142">Du kan fortsette å lage formatet ved å bruke noen av elementene som nødvendig roten av datamodellen.</span><span class="sxs-lookup"><span data-stu-id="3bf26-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="3bf26-143">En manglende tilordning av modellen for valgte rotelementet hindre ikke deg i å fortsette.</span><span class="sxs-lookup"><span data-stu-id="3bf26-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="3bf26-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3bf26-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="3bf26-145">Legg til en ny ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3bf26-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="3bf26-146">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="3bf26-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="3bf26-147">I feltet Ny angir du Modeltilordning basert på datamodellen Betalingsmodell (fiktiv).</span><span class="sxs-lookup"><span data-stu-id="3bf26-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="3bf26-148">I Navn-feltet skriver du inn "Betalingingsmodelltilordninger (fiktive)".</span><span class="sxs-lookup"><span data-stu-id="3bf26-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="3bf26-149">Betalingsmodelltilordninger (fiktive)</span><span class="sxs-lookup"><span data-stu-id="3bf26-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="3bf26-150">Angi eller velg en verdi i feltet Definisjon av datamodell.</span><span class="sxs-lookup"><span data-stu-id="3bf26-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="3bf26-151">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3bf26-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="3bf26-152">Utforme ER-modelltilordninger</span><span class="sxs-lookup"><span data-stu-id="3bf26-152">Design ER model mappings</span></span>
1. <span data-ttu-id="3bf26-153">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="3bf26-153">Click Designer.</span></span>
    * <span data-ttu-id="3bf26-154">Bruk ER designer til å angi modelltilordningene for de nødvendige rotelementene.</span><span class="sxs-lookup"><span data-stu-id="3bf26-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="3bf26-155">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="3bf26-155">Click Designer.</span></span>
    * <span data-ttu-id="3bf26-156">Simuler innstillingen for den valgte modelltilordningen for rotelementet til den valgte modellen.</span><span class="sxs-lookup"><span data-stu-id="3bf26-156">Simulate setting of selected model mapping for the selected model's root item.</span></span>  
3. <span data-ttu-id="3bf26-157">Velg Dynamics 365 for Operations\Tabellposter i treet.</span><span class="sxs-lookup"><span data-stu-id="3bf26-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="3bf26-158">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="3bf26-158">Click Add root.</span></span>
5. <span data-ttu-id="3bf26-159">I Navn-feltet skriver du inn "Finans".</span><span class="sxs-lookup"><span data-stu-id="3bf26-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="3bf26-160">Skriv inn 'LedgerJournalTrans' i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="3bf26-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="3bf26-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="3bf26-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="3bf26-162">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3bf26-162">Click OK.</span></span>
8. <span data-ttu-id="3bf26-163">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3bf26-163">Click Save.</span></span>
9. <span data-ttu-id="3bf26-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3bf26-164">Close the page.</span></span>
10. <span data-ttu-id="3bf26-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3bf26-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="3bf26-166">Start for å angi en annen ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3bf26-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="3bf26-167">Velg Betalingsmodell (fiktiv) i treet.</span><span class="sxs-lookup"><span data-stu-id="3bf26-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="3bf26-168">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="3bf26-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="3bf26-169">I feltet Ny angir du Format basert på datamodellen Betalingsmodell (fiktiv).</span><span class="sxs-lookup"><span data-stu-id="3bf26-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="3bf26-170">Angi eller velg en verdi i feltet Definisjon av datamodell.</span><span class="sxs-lookup"><span data-stu-id="3bf26-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="3bf26-171">Merk at nå er det bare ett rotelement som er tilgjengelig til å tilordne til datakildene til programmet.</span><span class="sxs-lookup"><span data-stu-id="3bf26-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="3bf26-172">Når minst én modelltilordning er introdusert, kan bare modellens rotelementer som er tilordnet til programmets datakilder, velges som en modelldefinisjon når ER-formatet er lagt til.</span><span class="sxs-lookup"><span data-stu-id="3bf26-172">When at least one model mapping is introduced, only the model's root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="3bf26-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3bf26-173">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]