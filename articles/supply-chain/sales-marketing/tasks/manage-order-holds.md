---
title: Behandle ordresperrer
description: Denne fremgangsmåten forklarer hvordan du plasserer salgsordrer for kunden på vent, hvordan du arbeider med ordresperreutsjekkinger og fjerner ordresperrer.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad19ff166c15748b7bbb4b82ef71dbf3e1e8ebd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "323968"
---
# <a name="manage-order-holds"></a><span data-ttu-id="12f6b-103">Behandle ordresperrer</span><span class="sxs-lookup"><span data-stu-id="12f6b-103">Manage order holds</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12f6b-104">Denne fremgangsmåten forklarer hvordan du plasserer salgsordrer for kunden på vent, hvordan du arbeider med ordresperreutsjekkinger og fjerner ordresperrer.</span><span class="sxs-lookup"><span data-stu-id="12f6b-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="12f6b-105">En ordre kan settes på vent av en rekke ulike årsaker.</span><span class="sxs-lookup"><span data-stu-id="12f6b-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="12f6b-106">Du kan for eksempel sperre en ordre til kundens adresse eller betalingsmetode kan bekreftes, eller til en leder kan gå gjennom kundens kredittgrense.</span><span class="sxs-lookup"><span data-stu-id="12f6b-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="12f6b-107">Mens ordren er på vent, kan den ikke behandles av lageret for forsendelse.</span><span class="sxs-lookup"><span data-stu-id="12f6b-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="12f6b-108">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="12f6b-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="12f6b-109">Definer ordresperrer</span><span class="sxs-lookup"><span data-stu-id="12f6b-109">Set up order holds</span></span>
1. <span data-ttu-id="12f6b-110">Gå til Salg og markedsføring > Oppsett > Salgsordrer > Ordresperrekoder.</span><span class="sxs-lookup"><span data-stu-id="12f6b-110">Go to Sales and marketing > Setup > Sales orders > Order hold codes.</span></span>
2. <span data-ttu-id="12f6b-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="12f6b-111">Click New.</span></span>
3. <span data-ttu-id="12f6b-112">Skriv inn en verdi i Sperrekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="12f6b-112">In the Hold code field, type a value.</span></span>
    * <span data-ttu-id="12f6b-113">Skriv for eksempel Ring tilbake.</span><span class="sxs-lookup"><span data-stu-id="12f6b-113">For example, type Call back.</span></span>  
4. <span data-ttu-id="12f6b-114">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="12f6b-114">In the Description field, type a value.</span></span>
    * <span data-ttu-id="12f6b-115">For eksempel Ordre sperret i påvente av at kunden ringer tilbake.</span><span class="sxs-lookup"><span data-stu-id="12f6b-115">For example, Order held waiting for customer callback.</span></span>  
    * <span data-ttu-id="12f6b-116">Eventuelt kan du merke av for Fjernede reservasjoner for å fjerne fysiske reservasjoner fra ordren når denne sperrekoden legges til.</span><span class="sxs-lookup"><span data-stu-id="12f6b-116">Optionally, select the Remove reservations check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="12f6b-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="12f6b-117">Click Save.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="12f6b-118">Sett ordre på vent</span><span class="sxs-lookup"><span data-stu-id="12f6b-118">Place order on hold</span></span>
1. <span data-ttu-id="12f6b-119">Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="12f6b-119">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="12f6b-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="12f6b-120">Click New.</span></span>
3. <span data-ttu-id="12f6b-121">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="12f6b-121">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="12f6b-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="12f6b-122">Click OK.</span></span>
5. <span data-ttu-id="12f6b-123">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="12f6b-123">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="12f6b-124">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="12f6b-124">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="12f6b-125">Klikk Salgsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="12f6b-125">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="12f6b-126">Klikk Ordresperrer.</span><span class="sxs-lookup"><span data-stu-id="12f6b-126">Click Order holds.</span></span>
9. <span data-ttu-id="12f6b-127">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="12f6b-127">Click New.</span></span>
10. <span data-ttu-id="12f6b-128">Velg koden du har opprettet i den forrige underoppgaven, i Sperrekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="12f6b-128">In the Hold code field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="12f6b-129">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="12f6b-129">Click Save.</span></span>
12. <span data-ttu-id="12f6b-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="12f6b-130">Close the page.</span></span>
13. <span data-ttu-id="12f6b-131">Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="12f6b-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
14. <span data-ttu-id="12f6b-132">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="12f6b-132">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="12f6b-133">Ordrer som er på vent, har feltene "Ikke behandle" og "Vent" merket av.</span><span class="sxs-lookup"><span data-stu-id="12f6b-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>    
15. <span data-ttu-id="12f6b-134">Klikk Plukk og pakk i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="12f6b-134">On the Action Pane, click Pick and pack.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="12f6b-135">Behandle ordresperrer</span><span class="sxs-lookup"><span data-stu-id="12f6b-135">Manage order holds</span></span>
1. <span data-ttu-id="12f6b-136">Gå til Salg og markedsføring > Salgsordrer > Åpne ordrer > Ordresperrer.</span><span class="sxs-lookup"><span data-stu-id="12f6b-136">Go to Sales and marketing > Sales orders > Open orders > Order holds.</span></span>
    * <span data-ttu-id="12f6b-137">Siden Ordresperrer fungerer som et arbeidsområde der du kan få en oversikt over alle gjeldende og behandlede sperrer, og behandle dem og tilknyttede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="12f6b-137">Order holds page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>      
2. <span data-ttu-id="12f6b-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="12f6b-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="12f6b-139">Klikk Sperre - utsjekking i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="12f6b-139">On the Action Pane, click Hold checkout.</span></span>
4. <span data-ttu-id="12f6b-140">Klikk Sjekk ut.</span><span class="sxs-lookup"><span data-stu-id="12f6b-140">Click Check out.</span></span>
5. <span data-ttu-id="12f6b-141">Fjern merket for den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="12f6b-141">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="12f6b-142">Feltet Sjekk ut til viser nå bruker-IDen din.</span><span class="sxs-lookup"><span data-stu-id="12f6b-142">The Checkout out to field now shows your user ID.</span></span>   
6. <span data-ttu-id="12f6b-143">Klikk Fjern utsjekking.</span><span class="sxs-lookup"><span data-stu-id="12f6b-143">Click Clear checkout.</span></span>
7. <span data-ttu-id="12f6b-144">Klikk Fjern sperre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="12f6b-144">On the Action Pane, click Clear hold.</span></span>
    * <span data-ttu-id="12f6b-145">Når du er klar til å fjerne sperren og la ordren gå videre til neste trinn i fullføringen, må du fjerne sperren.</span><span class="sxs-lookup"><span data-stu-id="12f6b-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="12f6b-146">Hvis ordren ikke krever noen endringer, kan du kjøre Fjern sperrer-handlingen.</span><span class="sxs-lookup"><span data-stu-id="12f6b-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="12f6b-147">Du kan imidlertid bruke Fjern og endre-handlingen hvis ordren må oppdateres når du fjerner en sperre.</span><span class="sxs-lookup"><span data-stu-id="12f6b-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    * <span data-ttu-id="12f6b-148">Fjern og send-handlingen gjelder bare når du bruker Telefonsenterfunksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="12f6b-148">The Clear and submit action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="12f6b-149">Klikk Fjern sperrer.</span><span class="sxs-lookup"><span data-stu-id="12f6b-149">Click Clear holds.</span></span>
    * <span data-ttu-id="12f6b-150">Sperringen er nå fjernet fra ordren og fjernet fra listen over aktive sperringer.</span><span class="sxs-lookup"><span data-stu-id="12f6b-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="12f6b-151">Hvis du vil se alle sperringene eller delsettet i henhold til en bestemt status, kan du endre verdien i Vis-feltet.</span><span class="sxs-lookup"><span data-stu-id="12f6b-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

