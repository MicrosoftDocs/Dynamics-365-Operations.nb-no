---
title: Behandle ordresperrer
description: Denne fremgangsmåten forklarer hvordan du plasserer salgsordrer for kunden på vent, hvordan du arbeider med ordresperreutsjekkinger og fjerner ordresperrer.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: edb3c6941af132f9ea1bf9f52f94cd6acc008d6c
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830062"
---
# <a name="manage-order-holds"></a><span data-ttu-id="cbdf3-103">Behandle ordresperrer</span><span class="sxs-lookup"><span data-stu-id="cbdf3-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cbdf3-104">Denne fremgangsmåten forklarer hvordan du plasserer salgsordrer for kunden på vent, hvordan du arbeider med ordresperreutsjekkinger og fjerner ordresperrer.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="cbdf3-105">En ordre kan settes på vent av en rekke ulike årsaker.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="cbdf3-106">Du kan for eksempel sperre en ordre til kundens adresse eller betalingsmetode kan bekreftes, eller til en leder kan gå gjennom kundens kredittgrense.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="cbdf3-107">Mens ordren er på vent, kan den ikke behandles av lageret for forsendelse.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="cbdf3-108">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="cbdf3-109">Definer ordresperrer</span><span class="sxs-lookup"><span data-stu-id="cbdf3-109">Set up order holds</span></span>
1. <span data-ttu-id="cbdf3-110">Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Oppsett > Salgsordrer > Ordresperrekoder**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="cbdf3-111">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-111">Click **New**.</span></span>
3. <span data-ttu-id="cbdf3-112">Skriv inn en verdi i **Sperrekode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="cbdf3-113">Skriv for eksempel inn Ring tilbake.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="cbdf3-114">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="cbdf3-115">For eksempel Ordre sperret i påvente av at kunden ringer tilbake.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="cbdf3-116">Du kan også merke av for **Fjernede reservasjoner** for å fjerne fysiske reservasjoner fra ordren når denne sperrekoden legges til.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="cbdf3-117">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="cbdf3-118">Sett ordre på vent</span><span class="sxs-lookup"><span data-stu-id="cbdf3-118">Place order on hold</span></span>
1. <span data-ttu-id="cbdf3-119">Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Salgsordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="cbdf3-120">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-120">Click **New**.</span></span>
3. <span data-ttu-id="cbdf3-121">Angi eller velg en verdi i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="cbdf3-122">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-122">Click **OK**.</span></span>
5. <span data-ttu-id="cbdf3-123">Angi eller velg en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="cbdf3-124">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="cbdf3-125">Klikk på **Salgsordre** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="cbdf3-126">Klikk på **Ordresperrer**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="cbdf3-127">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-127">Click **New**.</span></span>
10. <span data-ttu-id="cbdf3-128">Velg koden du har opprettet i den forrige underoppgaven, i **Sperrekode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="cbdf3-129">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-129">Click **Save**.</span></span>
12. <span data-ttu-id="cbdf3-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-130">Close the page.</span></span>
13. <span data-ttu-id="cbdf3-131">Gå til **Salg og markedsføring > Salgsordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="cbdf3-132">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-132">In the list, mark the selected row.</span></span> <span data-ttu-id="cbdf3-133">Ordrer som er på vent, har feltene "Ikke behandle" og "Vent" merket av.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="cbdf3-134">Klikk på **Plukk og pakk** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="cbdf3-135">Behandle ordresperrer</span><span class="sxs-lookup"><span data-stu-id="cbdf3-135">Manage order holds</span></span>
1. <span data-ttu-id="cbdf3-136">Gå til **Salg og markedsføring > Salgsordrer > Åpne ordrer > Ordresperrer**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="cbdf3-137">Siden **Ordresperrer** fungerer som et arbeidsområde der du kan få en oversikt over alle gjeldende og behandlede sperrer, og behandle dem og tilknyttede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="cbdf3-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="cbdf3-139">Klikk på **Sperre - utsjekking** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="cbdf3-140">Klikk på **Sjekk ut**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-140">Click **Check out**.</span></span>
5. <span data-ttu-id="cbdf3-141">Fjern merket for den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="cbdf3-142">Feltet **Sjekk ut til** viser nå bruker-ID-en din.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="cbdf3-143">Klikk på **Fjern utsjekking**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="cbdf3-144">Klikk på **Fjern sperre** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="cbdf3-145">Når du er klar til å fjerne sperren og la ordren gå videre til neste trinn i fullføringen, må du fjerne sperren.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="cbdf3-146">Hvis ordren ikke krever noen endringer, kan du kjøre Fjern sperrer-handlingen.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="cbdf3-147">Du kan imidlertid bruke Fjern og endre-handlingen hvis ordren må oppdateres når du fjerner en sperre.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="cbdf3-148">**Fjern og send**-handlingen gjelder bare når du bruker Telefonsenterfunksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="cbdf3-149">Klikk på **Fjern sperrer**.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-149">Click **Clear holds**.</span></span> <span data-ttu-id="cbdf3-150">Sperringen er nå fjernet fra ordren og fjernet fra listen over aktive sperringer.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="cbdf3-151">Hvis du vil se alle sperringene eller delsettet i henhold til en bestemt status, kan du endre verdien i Vis-feltet.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

