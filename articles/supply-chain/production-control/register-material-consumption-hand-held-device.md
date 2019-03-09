---
title: Registrere materialforbruk med en mobil enhet
description: Dette emnet beskriver en arbeidsflyt som aktiverer registrering av råvareforbruk i produksjonen ved hjelp av en håndholdt enhet.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5b9c73cf9b23eb8ad9ed872b76b92b395609e9a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "336135"
---
# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="0bcae-103">Registrere materialforbruk med en mobil enhet</span><span class="sxs-lookup"><span data-stu-id="0bcae-103">Register material consumption using a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bcae-104">Dette emnet beskriver en arbeidsflyt som aktiverer registrering av råvareforbruk i produksjonen ved hjelp av en håndholdt enhet.</span><span class="sxs-lookup"><span data-stu-id="0bcae-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="0bcae-105">Introduksjon</span><span class="sxs-lookup"><span data-stu-id="0bcae-105">Introduction</span></span>
------------

<span data-ttu-id="0bcae-106">Denne arbeidsflyten er relevant hvis det er strenge krav til sporbarhet for materialer.</span><span class="sxs-lookup"><span data-stu-id="0bcae-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="0bcae-107">For å vedlikeholde sporbarhet av materialet må det nøyaktige tidspunktet og antallet rapporteres for forbruk i slike tilfeller.</span><span class="sxs-lookup"><span data-stu-id="0bcae-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="0bcae-108">Denne prosessen kan ses i motsetning til pre- eller backflushing-operasjoner, der det er en forskyvning mellom tidspunktet for registrering og tidspunktet når det faktiske forbruket finner sted.</span><span class="sxs-lookup"><span data-stu-id="0bcae-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="0bcae-109">Dette emnet forklarer hvorfor en strategi for automatisk forbruk ikke kan brukes for noen materialer med krav til sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="0bcae-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="0bcae-110">La oss se på et enkelt scenario som forklarer hvordan du konfigurerer en arbeidsflyt for å aktivere registrering av råvareforbruk i produksjonen ved hjelp av en håndholdt enhet.</span><span class="sxs-lookup"><span data-stu-id="0bcae-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="0bcae-111">[![opprett en arbeidsflyt for å aktivere registrering av råmaterialforbruk ved å bruke en håndholdt enhet](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="0bcae-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="0bcae-112">Scenariodetaljer</span><span class="sxs-lookup"><span data-stu-id="0bcae-112">Scenario details</span></span>

<span data-ttu-id="0bcae-113">En fortløpende produksjonsprosess (5) bruker partikontrollert råmateriale RM-100.</span><span class="sxs-lookup"><span data-stu-id="0bcae-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="0bcae-114">Materialet er på lager på lokasjonen Bulk-001 (1) på nummerskilt PL-1 med to partier, B1 og B2, begge med et antall på 100 kilo.</span><span class="sxs-lookup"><span data-stu-id="0bcae-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="0bcae-115">Lagerarbeid (2) er frigitt og behandlet for RM-100, og materialet er plukket fra Bulk-001 til produksjonsinnleveringssted PIL-01 (3), som er definert som ikke-nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="0bcae-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="0bcae-116">Maskinoperatøren veier ut materialer fra produksjonsinnleveringsstedet (3) og registrerer vekten og partinummeret som er brukt (4).</span><span class="sxs-lookup"><span data-stu-id="0bcae-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="0bcae-117">Fra produksjonsinnleveringsstedet legges en del av materialet manuelt til produksjonsprosessen i definerte tidsintervaller.</span><span class="sxs-lookup"><span data-stu-id="0bcae-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="0bcae-118">Når maskinoperatøren legger til materiale, veies det på en vekt og partinummeret registreres.</span><span class="sxs-lookup"><span data-stu-id="0bcae-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-theworkflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="0bcae-119">Definer arbeidsflyten for å registrere forbruk ved hjelp av en håndholdt enhet</span><span class="sxs-lookup"><span data-stu-id="0bcae-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="0bcae-120">Opprett et ferdigvareprodukt, FG-100, med en stykkliste som har det partikontrollerte råmaterialet RM-100.</span><span class="sxs-lookup"><span data-stu-id="0bcae-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="0bcae-121">Legg til to partier, B1 og B2, av RM-100 i et antall på 100 til lokasjon: Bulk-001 på nummerskilt: PL-1.</span><span class="sxs-lookup"><span data-stu-id="0bcae-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="0bcae-122">Trekkprinsippet på stykklistelinjen for RM-100 er satt til **manuell**.</span><span class="sxs-lookup"><span data-stu-id="0bcae-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="0bcae-123">Angi produksjonsinnleveringsstedet til PIL-01.</span><span class="sxs-lookup"><span data-stu-id="0bcae-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="0bcae-124">Du kan gjøre dette ved å velge denne lokasjonen som standard produksjonsinnleveringssted på lager 51.</span><span class="sxs-lookup"><span data-stu-id="0bcae-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="0bcae-125">Opprett et nytt menyelement for mobilenhet:</span><span class="sxs-lookup"><span data-stu-id="0bcae-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="0bcae-126">**Menyelementnavn** - Register materialforbruk.</span><span class="sxs-lookup"><span data-stu-id="0bcae-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="0bcae-127">**Tittel** - Registrer materialforbruk.</span><span class="sxs-lookup"><span data-stu-id="0bcae-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="0bcae-128">**Modus** - Indirekte.</span><span class="sxs-lookup"><span data-stu-id="0bcae-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="0bcae-129">**Aktivitetskode** - Registrer materialforbruk.</span><span class="sxs-lookup"><span data-stu-id="0bcae-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="0bcae-130">Legg til menyelementet på **Produksjonsmobil**-enhetsmenyen.</span><span class="sxs-lookup"><span data-stu-id="0bcae-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="0bcae-131">Opprett en produksjonsordre for det ferdige produktet:</span><span class="sxs-lookup"><span data-stu-id="0bcae-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="0bcae-132">**Varenummer** - FG-100</span><span class="sxs-lookup"><span data-stu-id="0bcae-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="0bcae-133">**Område** - 5</span><span class="sxs-lookup"><span data-stu-id="0bcae-133">**Site** - 5</span></span> 
-    <span data-ttu-id="0bcae-134">**Lager** - 51</span><span class="sxs-lookup"><span data-stu-id="0bcae-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="0bcae-135">**Antall** - 150</span><span class="sxs-lookup"><span data-stu-id="0bcae-135">**Quantity** - 150</span></span>

<span data-ttu-id="0bcae-136">Produksjonsordren blir **estimert** og **frigitt** og lagerarbeid opprettes.</span><span class="sxs-lookup"><span data-stu-id="0bcae-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="0bcae-137">Fullfør arbeidet ved hjelp av arbeidsflyten for råvareplukking for den håndholdte enheten.</span><span class="sxs-lookup"><span data-stu-id="0bcae-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="0bcae-138">Dette tar materialet fra bulklokasjonen til produksjonsinnleveringsstedet PIL-01.</span><span class="sxs-lookup"><span data-stu-id="0bcae-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="0bcae-139">Når arbeidet er fullført, har materialet statusen **Plukket på produksjonsinnleveringsstedet**.</span><span class="sxs-lookup"><span data-stu-id="0bcae-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="0bcae-140">Statusen etter at arbeidet er behandlet, kan være enten **plukket** eller **fysisk reservert**.</span><span class="sxs-lookup"><span data-stu-id="0bcae-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="0bcae-141">Dette er konfigurert med parameteren **Avgangsstatus etter plassering i lager-skjema**.</span><span class="sxs-lookup"><span data-stu-id="0bcae-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="0bcae-142">Start produksjonsordren fra klienten eller den håndholdte enheten ved hjelp av menyelementet **Produksjonsstart**.</span><span class="sxs-lookup"><span data-stu-id="0bcae-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="0bcae-143">Etter at produksjonsordren er startet, kan du registrere materialforbruk i arbeidsflyten for den håndholdte enheten.</span><span class="sxs-lookup"><span data-stu-id="0bcae-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="0bcae-144">La oss begynne med å registrere forbruk på 25 kilo av parti B1.</span><span class="sxs-lookup"><span data-stu-id="0bcae-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="0bcae-145">Velg menyelementet **Registrer material** **forbruk** på menyen for den håndholdte enheten, og angi følgende detaljer:</span><span class="sxs-lookup"><span data-stu-id="0bcae-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="0bcae-146">Produksjonsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="0bcae-146">The production order number.</span></span> 
-    <span data-ttu-id="0bcae-147">Lokasjonen der materialet skal forbrukes, i dette tilfellet PIL-01.</span><span class="sxs-lookup"><span data-stu-id="0bcae-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="0bcae-148">Varenummer RM-100.</span><span class="sxs-lookup"><span data-stu-id="0bcae-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="0bcae-149">Partinummer B1.</span><span class="sxs-lookup"><span data-stu-id="0bcae-149">Batch number B1.</span></span> 
-    <span data-ttu-id="0bcae-150">Et antall på 25.</span><span class="sxs-lookup"><span data-stu-id="0bcae-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="0bcae-151">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0bcae-151">Select **OK**.</span></span>

<span data-ttu-id="0bcae-152">Legg merke til at meldingen "Journallinje er opprettet" vises på skjermen.</span><span class="sxs-lookup"><span data-stu-id="0bcae-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="0bcae-153">På produksjonsordren finnes det en åpen journal av typen **Produksjonsplukkliste** for varenummer RM-100 og partinummer B1.</span><span class="sxs-lookup"><span data-stu-id="0bcae-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="0bcae-154">Du kan nå velge å fortsette registreringen, for eksempel på partinummeret B2, og hver gang du velger **OK,** legges en ny journallinje til i den åpne journalen.</span><span class="sxs-lookup"><span data-stu-id="0bcae-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="0bcae-155">Når du er ferdig med registreringen, velger du **Ferdig** for å postere journalen og avslutte arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="0bcae-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="0bcae-156">Ekstra kommentarer</span><span class="sxs-lookup"><span data-stu-id="0bcae-156">Additional comments</span></span> 

-   <span data-ttu-id="0bcae-157">Hvis en bruker avbryter arbeidsflyten når en journallinje er opprettet, er journalen i en ikke-postert tilstand, men hvis brukeren senere bruker arbeidsflyten for samme produksjonsordre, blir linjene lagt til i den åpne journalen i stedet for en ny journal.</span><span class="sxs-lookup"><span data-stu-id="0bcae-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="0bcae-158">Den nye arbeidsflyten støtter også registrering av serienumre.</span><span class="sxs-lookup"><span data-stu-id="0bcae-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="0bcae-159">Det er bare mulig å registrere et varenummer som er definert i stykklisten eller formelen for den valgte produksjonsordren eller partiordren.</span><span class="sxs-lookup"><span data-stu-id="0bcae-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="0bcae-160">Materiale kan overforbrukes.</span><span class="sxs-lookup"><span data-stu-id="0bcae-160">Material can be overconsumed.</span></span> <span data-ttu-id="0bcae-161">Hvis for eksempel materialet er beregnet til bruk med et antall på 100 kilo, kan det bli overforbrukt med et antall på for eksempel 105 kilo.</span><span class="sxs-lookup"><span data-stu-id="0bcae-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>


