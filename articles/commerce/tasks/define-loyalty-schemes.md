---
title: " Definere fordelsskjemaer"
description: Denne prosedyren hjelper med å definere en fordelsplan.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a681a369a55a45692979e8e6f24f9c4018e00677
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023537"
---
# <a name="define-loyalty-schemes"></a><span data-ttu-id="82b61-103"> Definere fordelsskjemaer</span><span class="sxs-lookup"><span data-stu-id="82b61-103">Define loyalty schemes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="82b61-104">Denne prosedyren hjelper med å definere en fordelsplan.</span><span class="sxs-lookup"><span data-stu-id="82b61-104">This procedure walks through how to define a loyalty scheme.</span></span> <span data-ttu-id="82b61-105">Fordelsplaner er fordelsopptjenings- og innløsingsregler for et fordelsprogram.</span><span class="sxs-lookup"><span data-stu-id="82b61-105">Loyalty schemes are reward earning and redeeming rules for a loyalty program.</span></span> <span data-ttu-id="82b61-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="82b61-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="82b61-107">Gå til Detaljhandel og handel > Kunder > Fordel > Fordelsplaner.</span><span class="sxs-lookup"><span data-stu-id="82b61-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty schemes.</span></span>
2. <span data-ttu-id="82b61-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="82b61-108">Click New.</span></span>
3. <span data-ttu-id="82b61-109">Skriv inn en verdi i feltet Plan-ID.</span><span class="sxs-lookup"><span data-stu-id="82b61-109">In the Scheme ID field, type a value.</span></span>
4. <span data-ttu-id="82b61-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="82b61-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82b61-111">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="82b61-111">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="82b61-112">Du kan ha flere fordelsplaner for et fordelsprogram.</span><span class="sxs-lookup"><span data-stu-id="82b61-112">You can have multiple loyalty schemes for a loyalty program.</span></span> <span data-ttu-id="82b61-113">Fordelsplaner kan være for alle kanalene eller bare et delsett av kanalene.</span><span class="sxs-lookup"><span data-stu-id="82b61-113">Loyalty schemes can be for all channels or only a sub-set of channels.</span></span>  
6. <span data-ttu-id="82b61-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="82b61-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="82b61-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82b61-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="82b61-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="82b61-116">Click Save.</span></span>
9. <span data-ttu-id="82b61-117">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="82b61-117">Click Add line.</span></span>
10. <span data-ttu-id="82b61-118">Velg et alternativ i feltet Aktivitetstype.</span><span class="sxs-lookup"><span data-stu-id="82b61-118">In the Activity type field, select an option.</span></span>
    * <span data-ttu-id="82b61-119">Velg Kjøp av produkter basert på beløp hvis du vil at kundene skal oppnå fordeler basert på hvor mye de bruker.</span><span class="sxs-lookup"><span data-stu-id="82b61-119">Select Purchase products by amount if you want customers to earn rewards based on how much they spend.</span></span> <span data-ttu-id="82b61-120">Velg Kjøp av produkter basert på antall hvis du vil at kundene skal oppnå fordeler basert på hvor mange produkter de kjøper.</span><span class="sxs-lookup"><span data-stu-id="82b61-120">Select Purchase products by quantity if you want customers to earn rewards based on how many products they buy.</span></span>  <span data-ttu-id="82b61-121">Velg Antall salgstransaksjoner hvis du vil at kundene skal opptjene fordeler for alle salgstransaksjoner uansett hva eller hvor mye som kjøpes.</span><span class="sxs-lookup"><span data-stu-id="82b61-121">Select Sales transaction count if you want customers to earn rewards for each sales transaction, regardless of what or how much is purchased.</span></span>  
    * <span data-ttu-id="82b61-122">Velg en kategori.</span><span class="sxs-lookup"><span data-stu-id="82b61-122">Select a category.</span></span> <span data-ttu-id="82b61-123">Kategorien begrenser hvilke produkter opptjeningsregelen gjelder for.</span><span class="sxs-lookup"><span data-stu-id="82b61-123">The category will limit which products this earning rule applies to.</span></span>  
    * <span data-ttu-id="82b61-124">Hvis du vil at opptjeningsregelen skal gjelde for alle produkter, lar du feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="82b61-124">If you want the earning rule to apply to all products, leave this field blank.</span></span>  
11. <span data-ttu-id="82b61-125">Angi et tall i feltet Beløp/antall for aktivitet.</span><span class="sxs-lookup"><span data-stu-id="82b61-125">In the Activity amount/quantity field, enter a number.</span></span>
    *  <span data-ttu-id="82b61-126">For aktivitetstypen Antall salgstransaksjoner bør du alltid bruke verdien 1,0.</span><span class="sxs-lookup"><span data-stu-id="82b61-126">For activity type Sales transaction count, you should always use a value of '1.0'.</span></span> <span data-ttu-id="82b61-127">For aktivitetstypene Kjøp av produkter basert på beløp eller Kjøp av produkter basert på antall utløses ikke opptjeningsregelen hvis transaksjonen er lavere enn den angitte verdien.</span><span class="sxs-lookup"><span data-stu-id="82b61-127">For activity types of Purchase by amount or Purchase by quantity, any transaction that is less than the value entered will not trigger the earning rule.</span></span> <span data-ttu-id="82b61-128">Hvis for eksempel aktivitetstypen er Kjøp av produkter basert på beløp og du angir 10,00, vil ikke salgstransaksjonen på 9,00 opptjene fordeler for denne opptjeningsregelen.</span><span class="sxs-lookup"><span data-stu-id="82b61-128">For example, if the activity type is Purchase by amount, and you enter '10.00', then a sales transaction for '9.00' will not earn rewards for this earning rule.</span></span>  
12. <span data-ttu-id="82b61-129">Skriv inn en verdi i Aktivitetsvaluta-feltet.</span><span class="sxs-lookup"><span data-stu-id="82b61-129">In the Activity currency field, type a value.</span></span>
13. <span data-ttu-id="82b61-130">Klikk rullegardinknappen i feltet ID for fordelspoeng for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="82b61-130">In the Reward point ID field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="82b61-131">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82b61-131">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="82b61-132">Angi et tall i Fordelspoeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="82b61-132">In the Reward points field, enter a number.</span></span>
    * <span data-ttu-id="82b61-133">Fordelspoeng av typen beløp registrerer opptjente beløp i desimaler.</span><span class="sxs-lookup"><span data-stu-id="82b61-133">Amount type reward points will record earned amounts with decimals.</span></span> <span data-ttu-id="82b61-134">Hvis for eksempel opptjeningsregelen tilsier at du får 1 poeng for hver krone som brukes, og kunden bruker 1,25 kroner, får kunden 1,25 fordelspoeng.</span><span class="sxs-lookup"><span data-stu-id="82b61-134">For example, if the earning rule states 1 reward point earned for every 1 Canadian Dollar spent, and the customer spends 1.25 Canadian Dollars, then the customer will earn 1.25 reward points.</span></span> <span data-ttu-id="82b61-135">Fordelspoeng av typen antall registrerer opptjente beløp i heltall.</span><span class="sxs-lookup"><span data-stu-id="82b61-135">Quantity type reward points will record earned amounts in integers.</span></span> <span data-ttu-id="82b61-136">Hvis for eksempel opptjeningsregelen tilsier at du får 1 poeng for hver krone som brukes, og kunden bruker 1,25 kroner, får kunden 1,0 fordelspoeng.</span><span class="sxs-lookup"><span data-stu-id="82b61-136">Using the example where the earning rule states 1 reward point earned for every 1 Canadian Dollar spent, and the customer spends 1.25 Canadian Dollars, then the customer will earn 1.0 reward points.</span></span>  
16. <span data-ttu-id="82b61-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="82b61-137">Click Save.</span></span>
17. <span data-ttu-id="82b61-138">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="82b61-138">Click Add line.</span></span>
    * <span data-ttu-id="82b61-139">Innløsingsregler brukes når fordelsbetalingsmåten brukes.</span><span class="sxs-lookup"><span data-stu-id="82b61-139">Redemption rules are used when the loyalty payment method is used.</span></span>  
18. <span data-ttu-id="82b61-140">Klikk rullegardinknappen i feltet ID for fordelspoeng for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="82b61-140">In the Reward point ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="82b61-141">Det vises bare fordelspoeng som kan innløses.</span><span class="sxs-lookup"><span data-stu-id="82b61-141">Only redeemable reward points are shown.</span></span>  
19. <span data-ttu-id="82b61-142">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82b61-142">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="82b61-143">Angi et tall i Fordelspoeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="82b61-143">In the Reward points field, enter a number.</span></span>
21. <span data-ttu-id="82b61-144">Velg et alternativ i feltet Innløsingstype.</span><span class="sxs-lookup"><span data-stu-id="82b61-144">In the Redemption type field, select an option.</span></span>
    * <span data-ttu-id="82b61-145">Når du velger Betaling etter beløp, behandles feltet Beløp eller antall som en valutaverdi.</span><span class="sxs-lookup"><span data-stu-id="82b61-145">Selecting Payment by amount causes the Amount or quantity field to be treated as a currency value.</span></span> <span data-ttu-id="82b61-146">I dette tilfellet er beløpet for fordelspoeng som brukes per valutaenhet med betaling, et fast forholdstall.</span><span class="sxs-lookup"><span data-stu-id="82b61-146">In this case, the amount of reward points used per currency unit of payment is a fixed ratio.</span></span> <span data-ttu-id="82b61-147">Når du velger Betaling etter antall, behandles feltet Beløp eller antall som en antallsverdi.</span><span class="sxs-lookup"><span data-stu-id="82b61-147">Selecting Payment by quantity causes the Amount or quantity field to be treated as a quantity value.</span></span> <span data-ttu-id="82b61-148">I dette tilfellet er beløpet for fordelspoeng som brukes per vareantall, et fast forholdstall, men beløpet i valuta kan variere hvis prisen på varene som betales med fordelspoeng, varierer for samme antall.</span><span class="sxs-lookup"><span data-stu-id="82b61-148">In this case, the amount of reward points used per item quantity is a fixed ratio, however, the amount in currency can vary if the price of items paid for with loyalty reward points varies for the same quantity.</span></span> <span data-ttu-id="82b61-149">Innløsningstypen Rabatt for fordelspoeng er bare gyldig når konfigurasjonsnøkkelen for Russland under Land-/områdespesifikke funksjoner er aktivert, og ISO-koden er satt til RU under Funksjonalitetsprofiler for salgssted.</span><span class="sxs-lookup"><span data-stu-id="82b61-149">Redemption type of Loyalty points discount is only valid when the 'Russia' Country/Regional specific features configuration key is enabled, and the POS functionality profiles has an ISO code of 'RU'.</span></span>  
    * <span data-ttu-id="82b61-150">Velg en kategori.</span><span class="sxs-lookup"><span data-stu-id="82b61-150">Select a category.</span></span> <span data-ttu-id="82b61-151">Kategorien begrenser hvilke produkter innløsingsregelen gjelder for.</span><span class="sxs-lookup"><span data-stu-id="82b61-151">The category will limit which products this redemption rule applies to.</span></span>  
    * <span data-ttu-id="82b61-152">Hvis du vil at innløsingsregelen skal gjelde for alle produkter, lar du feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="82b61-152">If you want the redemption rule to apply to all products, leave this field blank.</span></span>  
22. <span data-ttu-id="82b61-153">Angi et tall i Beløp eller antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="82b61-153">In the Amount or quantity field, enter a number.</span></span>
23. <span data-ttu-id="82b61-154">Skriv inn en verdi i Valuta-feltet.</span><span class="sxs-lookup"><span data-stu-id="82b61-154">In the Currency field, type a value.</span></span>
24. <span data-ttu-id="82b61-155">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="82b61-155">Click Save.</span></span>
25. <span data-ttu-id="82b61-156">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="82b61-156">Click Add line.</span></span>
    * <span data-ttu-id="82b61-157">Velg en eller flere noder fra listen Tilgjengelige organisasjonsnoder og flytt dem til listen Valgte organisasjonsnoder ved å klikke pilen mellom de to listene.</span><span class="sxs-lookup"><span data-stu-id="82b61-157">Select one or more nodes from the Available organization nodes list and move them to the Selected organization nodes list by clicking the arrow between the two lists.</span></span>  
26. <span data-ttu-id="82b61-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="82b61-158">Click OK.</span></span>
27. <span data-ttu-id="82b61-159">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="82b61-159">Click Save.</span></span>
    * <span data-ttu-id="82b61-160">Hver gang du endrer kanaler for en fordelsplan, må du kjøre Behandle fordelsplaner.</span><span class="sxs-lookup"><span data-stu-id="82b61-160">Anytime you change the channels for a loyalty scheme, you must run Process loyalty schemes.</span></span> <span data-ttu-id="82b61-161">På denne måten får kanalene oppdaterte fordelsplaner.</span><span class="sxs-lookup"><span data-stu-id="82b61-161">That way, the channels will get updated loyalty schemes.</span></span>  
