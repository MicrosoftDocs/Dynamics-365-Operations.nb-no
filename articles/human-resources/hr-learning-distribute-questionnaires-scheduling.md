---
title: Distribuere spørreskjemaer ved hjelp av planlegging
description: Med planlegging av spørreskjema kan du planlegge og distribuere spørreskjemaer til flere respondenter.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 50be7631ec303171640b7fa9e6d283a198bd1a52
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465012"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="1ede8-103">Distribuere spørreskjemaer ved hjelp av planlegging</span><span class="sxs-lookup"><span data-stu-id="1ede8-103">Distribute questionnaires using scheduling</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1ede8-104">Med planlegging av spørreskjema kan du planlegge og distribuere spørreskjemaer til flere respondenter.</span><span class="sxs-lookup"><span data-stu-id="1ede8-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="1ede8-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="1ede8-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="1ede8-106">Opprette en spørreskjemaplan</span><span class="sxs-lookup"><span data-stu-id="1ede8-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="1ede8-107">Gå til Spørreskjema > Distribuer > Spørreskjemaplaner.</span><span class="sxs-lookup"><span data-stu-id="1ede8-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="1ede8-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="1ede8-108">Click New.</span></span>

3. <span data-ttu-id="1ede8-109">Skriv inn en verdi i feltet Planlegging.</span><span class="sxs-lookup"><span data-stu-id="1ede8-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="1ede8-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="1ede8-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1ede8-111">Sett planen til anonym hvis svarene skal registreres uten navn tilknyttet svaret.</span><span class="sxs-lookup"><span data-stu-id="1ede8-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="1ede8-112">Tillatelse av anonyme resultater må først defineres i parameterne for personal.</span><span class="sxs-lookup"><span data-stu-id="1ede8-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="1ede8-113">I Type-feltet velger du planleggingstypen.</span><span class="sxs-lookup"><span data-stu-id="1ede8-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="1ede8-114">I dette eksemplet bruker vi tilfredshetstypen.</span><span class="sxs-lookup"><span data-stu-id="1ede8-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="1ede8-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="1ede8-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="1ede8-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1ede8-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="1ede8-117">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ede8-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="1ede8-118">Vis E-post for ansattselvbetjening-delen.</span><span class="sxs-lookup"><span data-stu-id="1ede8-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="1ede8-119">Skriv inn en verdi i Emne-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ede8-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="1ede8-120">Eksempel: Spørreskjema tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="1ede8-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="1ede8-121">I Tekst-feltet skriver du inn brødteksten i e-postmeldingen.</span><span class="sxs-lookup"><span data-stu-id="1ede8-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="1ede8-122">Legg merke til at variabelen kan brukes til å erstatte verdier i systemet.</span><span class="sxs-lookup"><span data-stu-id="1ede8-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="1ede8-123">Eksempel: Kjære %P% Logg på Ansattselvbetjening for å fylle ut spørreskjemaet om ansattes helse.</span><span class="sxs-lookup"><span data-stu-id="1ede8-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="1ede8-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="1ede8-124">Contoso</span></span>  

12. <span data-ttu-id="1ede8-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="1ede8-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="1ede8-126">Bruk oppsettsdetaljene til å velge spørreskjemaet/spørreskjemaene som skal besvares, i tillegg til eventuelle spørringer som skal brukes til å velge respondenter.</span><span class="sxs-lookup"><span data-stu-id="1ede8-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="1ede8-127">Klikk Oppsettsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="1ede8-127">Click Setup details.</span></span>

2. <span data-ttu-id="1ede8-128">Velg en spørring som skal brukes for å søke etter respondenter for spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="1ede8-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="1ede8-129">Eksempel: Arbeidere</span><span class="sxs-lookup"><span data-stu-id="1ede8-129">Example: Workers</span></span>  

3. <span data-ttu-id="1ede8-130">Klikk Vis eller endre spørring for å velge bestemte personer eller endre spørringen for å finne personer som oppfyller bestemte vilkår.</span><span class="sxs-lookup"><span data-stu-id="1ede8-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="1ede8-131">Vær oppmerksom på at alle respondenter må også være brukere i systemet.</span><span class="sxs-lookup"><span data-stu-id="1ede8-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="1ede8-132">Merk raden for Person i listen.</span><span class="sxs-lookup"><span data-stu-id="1ede8-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="1ede8-133">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ede8-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="1ede8-134">Velg Julie Funderburk</span><span class="sxs-lookup"><span data-stu-id="1ede8-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="1ede8-135">Velg Julia Funderburk i listen.</span><span class="sxs-lookup"><span data-stu-id="1ede8-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="1ede8-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1ede8-136">Click OK.</span></span>

8. <span data-ttu-id="1ede8-137">Klikk kategorien Spørreskjemaer.</span><span class="sxs-lookup"><span data-stu-id="1ede8-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="1ede8-138">I treet utvider du "the node for the questionnaire type Satisfaction Survey".</span><span class="sxs-lookup"><span data-stu-id="1ede8-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="1ede8-139">Merk av for Workforce Health Assessment.</span><span class="sxs-lookup"><span data-stu-id="1ede8-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="1ede8-140">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1ede8-140">Click OK.</span></span>

12. <span data-ttu-id="1ede8-141">Klikk Planlagt svarøkt.</span><span class="sxs-lookup"><span data-stu-id="1ede8-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="1ede8-142">Legg merke til at planlagte svarøkter er opprettet for hver bruker som er valgt/spørres.</span><span class="sxs-lookup"><span data-stu-id="1ede8-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="1ede8-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1ede8-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="1ede8-144">Start spørreskjemaplanen for å gjøre spørreskjemaet tilgjengelig for respondentene.</span><span class="sxs-lookup"><span data-stu-id="1ede8-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="1ede8-145">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="1ede8-145">Click Functions.</span></span>

2. <span data-ttu-id="1ede8-146">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="1ede8-146">Click Start.</span></span>

3. <span data-ttu-id="1ede8-147">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1ede8-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="1ede8-148">Send e-post for å varsle svarpersoner om at spørreskjemaet er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="1ede8-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="1ede8-149">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="1ede8-149">Click Functions.</span></span>

2. <span data-ttu-id="1ede8-150">Klikk Send e-post.</span><span class="sxs-lookup"><span data-stu-id="1ede8-150">Click Send email.</span></span>

3. <span data-ttu-id="1ede8-151">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="1ede8-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="1ede8-152">Bruk planlagte svarøkter til å følge med på hvem som må fylle ut spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="1ede8-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="1ede8-153">Klikk Planlagt svarøkt.</span><span class="sxs-lookup"><span data-stu-id="1ede8-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="1ede8-154">Slett eventuelle gjenværende planlagte svarøkter når du er klar til å avslutte den planlagte økten.</span><span class="sxs-lookup"><span data-stu-id="1ede8-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="1ede8-155">Klikk Slett.</span><span class="sxs-lookup"><span data-stu-id="1ede8-155">Click Delete.</span></span>

3. <span data-ttu-id="1ede8-156">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="1ede8-156">Click Yes.</span></span>

4. <span data-ttu-id="1ede8-157">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1ede8-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="1ede8-158">Avslutt planleggingen når alle respondentene har fullført spørreskjemaet og /eller alle gjenstående planlagte svarøkter er slettet.</span><span class="sxs-lookup"><span data-stu-id="1ede8-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="1ede8-159">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="1ede8-159">Click Functions.</span></span>
2. <span data-ttu-id="1ede8-160">Klikk Avslutt.</span><span class="sxs-lookup"><span data-stu-id="1ede8-160">Click End.</span></span>
3. <span data-ttu-id="1ede8-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1ede8-161">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]