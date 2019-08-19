---
title: Registrere varer for en vare for avanserte lageraktiviteter ved hjelp av en journal for vareankomst
description: Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker avanserte lagerstyringsprosesser.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec15a5d35c360ed8f8eddffc44d303df193ce3e7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847276"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="67f87-103">Registrere varer for en vare for avanserte lageraktiviteter ved hjelp av en journal for vareankomst</span><span class="sxs-lookup"><span data-stu-id="67f87-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67f87-104">Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker avanserte lagerstyringsprosesser.</span><span class="sxs-lookup"><span data-stu-id="67f87-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="67f87-105">Dette gjøres vanligvis av en mottaksassistent.</span><span class="sxs-lookup"><span data-stu-id="67f87-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="67f87-106">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="67f87-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="67f87-107">Du må ha en bekreftet bestilling med en åpen bestillingslinje før du starter denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="67f87-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="67f87-108">Varen på linjen må lagres, og den må ikke bruke produktvarianter, og kan ikke ha sporingsdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="67f87-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="67f87-109">Og varene må være tilknyttet en lagringsdimensjonsgruppe som er aktivert for lagerstyringsprosess.</span><span class="sxs-lookup"><span data-stu-id="67f87-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="67f87-110">Lageret som brukes, må være aktivert for lagerprosjektstyringsprosesser, og lokasjonen som du bruker for mottak, må være nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="67f87-110">The warehouse that’s used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="67f87-111">Hvis du bruker USMF, kan du bruke firmakonto 1001, lager 51 og vare M9200 til å opprette din bestilling.</span><span class="sxs-lookup"><span data-stu-id="67f87-111">If you’re using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="67f87-112">Noter nummeret på bestillingen som du oppretter, og noter også varenummeret og området som du brukte for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="67f87-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="67f87-113">Opprette et hode for vareankomstjournal</span><span class="sxs-lookup"><span data-stu-id="67f87-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="67f87-114">Gå til Vareankomst.</span><span class="sxs-lookup"><span data-stu-id="67f87-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="67f87-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="67f87-115">Click New.</span></span>
3. <span data-ttu-id="67f87-116">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="67f87-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="67f87-117">Hvis du bruker USMF, kan du velge WHS.</span><span class="sxs-lookup"><span data-stu-id="67f87-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="67f87-118">Hvis du bruker andre data, må journalen med det valgte navnet ha følgende egenskaper: Kontroller plukklokasjon plukklokasjon må settes til Nei og Karantenestyring må settes til Nei.</span><span class="sxs-lookup"><span data-stu-id="67f87-118">If you’re using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="67f87-119">Skriv inn en verdi i Nummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="67f87-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="67f87-120">Skriv inn en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="67f87-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="67f87-121">Velg området som du brukte for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="67f87-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="67f87-122">Dette skal fungere som en standardverdi som vil være standard for alle linjene i journalen.</span><span class="sxs-lookup"><span data-stu-id="67f87-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="67f87-123">Hvis du har brukt lageret 51 USMF, kan du velge området 5.</span><span class="sxs-lookup"><span data-stu-id="67f87-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="67f87-124">Skriv inn en verdi i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="67f87-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="67f87-125">Velg et gyldig lager for området du har valgt.</span><span class="sxs-lookup"><span data-stu-id="67f87-125">Select a valid warehouse for the site that you’ve selected.</span></span> <span data-ttu-id="67f87-126">Dette skal fungere som en standardverdi som vil være standard for alle linjene i journalen.</span><span class="sxs-lookup"><span data-stu-id="67f87-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="67f87-127">Hvis du bruker eksempelverdiene i USMF, velger du 51.</span><span class="sxs-lookup"><span data-stu-id="67f87-127">If you’re using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="67f87-128">Skriv inn en verdi i feltet Lokasjon.</span><span class="sxs-lookup"><span data-stu-id="67f87-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="67f87-129">Velg en gyldig lokasjon i lageret du har valgt.</span><span class="sxs-lookup"><span data-stu-id="67f87-129">Select a valid location in the warehouse that you’ve selected.</span></span> <span data-ttu-id="67f87-130">Lokasjonen må være tilknyttet en lokasjonsprofil, som er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="67f87-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="67f87-131">Dette skal fungere som en standardverdi som vil være standard for alle linjene i journalen.</span><span class="sxs-lookup"><span data-stu-id="67f87-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="67f87-132">Hvis du bruker eksempelverdiene i USMF, velger du Bulk-008.</span><span class="sxs-lookup"><span data-stu-id="67f87-132">If you’re using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="67f87-133">Høyreklikk på rullegardinpilen i feltet Nummerskilt, og velg deretter Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="67f87-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="67f87-134">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="67f87-134">Click New.</span></span>
10. <span data-ttu-id="67f87-135">Skriv inn en verdi i feltet Nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="67f87-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="67f87-136">Noter verdien.</span><span class="sxs-lookup"><span data-stu-id="67f87-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="67f87-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="67f87-137">Click Save.</span></span>
12. <span data-ttu-id="67f87-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="67f87-138">Close the page.</span></span>
13. <span data-ttu-id="67f87-139">Skriv inn en verdi i feltet Nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="67f87-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="67f87-140">Angi verdien for nummerskiltet du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="67f87-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="67f87-141">Dette skal fungere som en standardverdi som vil være standard for alle linjene i journalen.</span><span class="sxs-lookup"><span data-stu-id="67f87-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="67f87-142">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="67f87-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="67f87-143">Legge til en linje</span><span class="sxs-lookup"><span data-stu-id="67f87-143">Add a line</span></span>
1. <span data-ttu-id="67f87-144">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="67f87-144">Click Add line.</span></span>
2. <span data-ttu-id="67f87-145">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="67f87-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="67f87-146">Angi varenummeret som du brukte på bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="67f87-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="67f87-147">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="67f87-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="67f87-148">Angi antallet du vil registrere.</span><span class="sxs-lookup"><span data-stu-id="67f87-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="67f87-149">Dato-feltet bestemmer hvilken dato når lagerbeholdningen for denne varen skal registreres i lageret.</span><span class="sxs-lookup"><span data-stu-id="67f87-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="67f87-150">Parti-ID-en fylles ut av systemet hvis den kan identifiseres unikt fra informasjonen.</span><span class="sxs-lookup"><span data-stu-id="67f87-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="67f87-151">Ellers må du legge den til manuelt.</span><span class="sxs-lookup"><span data-stu-id="67f87-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="67f87-152">Dette er et obligatorisk felt, som kobler denne registreringen til en bestemt kildedokumentlinje.</span><span class="sxs-lookup"><span data-stu-id="67f87-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="67f87-153">Fullføre registreringen</span><span class="sxs-lookup"><span data-stu-id="67f87-153">Complete the registration</span></span>
1. <span data-ttu-id="67f87-154">Klikk Valider.</span><span class="sxs-lookup"><span data-stu-id="67f87-154">Click Validate.</span></span>
    * <span data-ttu-id="67f87-155">Dette kontrollerer at journalen er klar for postering.</span><span class="sxs-lookup"><span data-stu-id="67f87-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="67f87-156">Hvis valideringen mislykkes, må du rette opp feilene før du kan postere journalen.</span><span class="sxs-lookup"><span data-stu-id="67f87-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="67f87-157">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="67f87-157">Click OK.</span></span>
    * <span data-ttu-id="67f87-158">Når du har klikket OK, kontrollerer du meldingen.</span><span class="sxs-lookup"><span data-stu-id="67f87-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="67f87-159">Det skal være en melding om at journalen er OK.</span><span class="sxs-lookup"><span data-stu-id="67f87-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="67f87-160">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="67f87-160">Click Post.</span></span>
4. <span data-ttu-id="67f87-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="67f87-161">Click OK.</span></span>
    * <span data-ttu-id="67f87-162">Når du har klikket OK, kontrollerer du meldingslinjen.</span><span class="sxs-lookup"><span data-stu-id="67f87-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="67f87-163">Det skal være en melding om at operasjonen er fullført.</span><span class="sxs-lookup"><span data-stu-id="67f87-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="67f87-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="67f87-164">Close the page.</span></span>

