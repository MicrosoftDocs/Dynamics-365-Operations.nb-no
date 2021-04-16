---
title: Registrere varer for en vare for avanserte lageraktiviteter ved hjelp av en journal for vareankomst
description: Dette emnet presenterer et scenario som viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker avanserte lagerstyringsprosesser.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830840"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="6fe5c-103">Registrere varer for en vare for avanserte lageraktiviteter ved hjelp av en journal for vareankomst</span><span class="sxs-lookup"><span data-stu-id="6fe5c-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6fe5c-104">Dette emnet presenterer et scenario som viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker avanserte lagerstyringsprosesser.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="6fe5c-105">Dette gjøres vanligvis av en mottaksassistent.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="6fe5c-106">Aktivere eksempeldata</span><span class="sxs-lookup"><span data-stu-id="6fe5c-106">Enable sample data</span></span>

<span data-ttu-id="6fe5c-107">Hvis du vil gå gjennom dette scenariet ved hjelp av eksempelpostene og verdiene som er angitt i dette emnet, må du bruke et system der standard demodata er installert, og du må velge den juridiske enheten *USMF* før du begynner.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="6fe5c-108">Du kan i stedet gå gjennom dette scenariet ved å erstatte verdier fra dine egne data hvis du har følgende data tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="6fe5c-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="6fe5c-109">Du må ha en bekreftet bestilling med en åpen bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="6fe5c-110">Varen på linjen må være lagerført.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-110">The item on the line must be stocked.</span></span> <span data-ttu-id="6fe5c-111">Den må ikke brukes produktvarianter og må ikke ha sporingsdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="6fe5c-112">Varen må være tilknyttet en lagringsdimensjonsgruppe som har lagerbehandlingsprosessen aktivert.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="6fe5c-113">Lageret som brukes, må være aktivert for lagerprosjektstyringsprosesser, og lokasjonen som du bruker for mottak, må være nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="6fe5c-114">Opprett et journalhode for vareankomst som bruker lagerstyring</span><span class="sxs-lookup"><span data-stu-id="6fe5c-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="6fe5c-115">Dette scenariet viser hvordan du oppretter et journalhode for vareankomst som bruker lagerbehandling:</span><span class="sxs-lookup"><span data-stu-id="6fe5c-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="6fe5c-116">Kontroller at systemet inneholder en bekreftet bestilling som oppfyller kravene som er beskrevet i den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="6fe5c-117">Dette scenariet bruker en bestilling for firmaet *USMF*, leverandørkontoen *1001*, lageret *51*, med en ordrelinje for *10 PL* (10 paller) med varenummer *M9200*.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="6fe5c-118">Noter deg bestillingsnummeret som du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="6fe5c-119">Gå til **Lagerstyring \> Loggoppføringer \> Vareankomst \> Vareankomst**.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="6fe5c-120">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="6fe5c-121">Dialogboksen **Opprett lagerbehandlingsjournal** åpnes.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="6fe5c-122">Velg et journalnavn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="6fe5c-123">Hvis du bruker *USMF*-eksempeldata, velger du *WHS*.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="6fe5c-124">Hvis du bruker dine egne data, må journalen du velger, ha **Kontroller plukklokasjon** satt til *Nei* og **Karantenestyring** satt til *Nei*.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="6fe5c-125">Angi **Referanse** til *Bestilling*.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="6fe5c-126">Angi **Kontonummer** til *1001*.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="6fe5c-127">Angi **Nummer** til nummeret på bestillingen som du identifiserte for denne øvelsen.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="6fe5c-128">![Vareankomstjournal](../media/item-arrival-journal-header.png "Vareankomstjournal")</span><span class="sxs-lookup"><span data-stu-id="6fe5c-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="6fe5c-129">Velg **OK** for å opprette journalhodet.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="6fe5c-130">I **Journallinjer**-delen velger du **Legg til linje** og angir følgende data:</span><span class="sxs-lookup"><span data-stu-id="6fe5c-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="6fe5c-131">**Varenummer** – Angi til *M9200*.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="6fe5c-132">**Sted**, **Lager** og **Antall** blir angitt basert på lagertransaksjonsdataene for de 10 pallene (1000 per stk.).</span><span class="sxs-lookup"><span data-stu-id="6fe5c-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="6fe5c-133">**Lokasjon** – Angi til *001*.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="6fe5c-134">Denne bestemte lokasjonen sporer ikke nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="6fe5c-135">![Vareankomstjournallinje](../media/item-arrival-journal-line.png "Vareankomstjournallinje")</span><span class="sxs-lookup"><span data-stu-id="6fe5c-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fe5c-136">**Dato**-feltet bestemmer hvilken dato når lagerbeholdningen for denne varen skal registreres i lageret.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="6fe5c-137">**Parti-ID** fylles ut av systemet hvis den kan identifiseres unikt fra informasjonen.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="6fe5c-138">Ellers må du angi den manuelt.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="6fe5c-139">Dette er et obligatorisk felt, som kobler denne registreringen til en bestemt kildedokumentlinje.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="6fe5c-140">Velg **Valider** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="6fe5c-141">Dette kontrollerer at journalen er klar for postering.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="6fe5c-142">Hvis valideringen mislykkes, må du rette opp feilene før du kan postere journalen.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="6fe5c-143">Dialogboksen **Kontroller journal** åpnes.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="6fe5c-144">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-144">Select **OK**.</span></span>
1. <span data-ttu-id="6fe5c-145">Gå gjennom meldingslinjen.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-145">Review the message bar.</span></span> <span data-ttu-id="6fe5c-146">Det skal være en melding om at operasjonen er fullført.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="6fe5c-147">Velg **Poster** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="6fe5c-148">Dialogboksen **Poster journal** åpnes.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="6fe5c-149">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-149">Select **OK**.</span></span>
1. <span data-ttu-id="6fe5c-150">Gå gjennom meldingslinjen.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-150">Review the message bar.</span></span> <span data-ttu-id="6fe5c-151">Det skal være meldinger om at operasjonen er fullført.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="6fe5c-152">Velg **Funksjoner > Produktmottak** i handlingsruten for å oppdatere bestillingslinjen og postere et produktmottak.</span><span class="sxs-lookup"><span data-stu-id="6fe5c-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
