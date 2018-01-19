---
title: Livssyklustilstand for produkt
description: Livssyklustilstand for produkter dokumenterer livssyklustilstanden til et frigitt produkt eller produktvariant.
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: cvocph
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 8337f1dfb938f9fa69924e77a25a68ee56dbd2ac
ms.contentlocale: nb-no
ms.lasthandoff: 01/19/2018

---

# <a name="product-lifecycle-state"></a><span data-ttu-id="958d4-103">Livssyklustilstand for produkt</span><span class="sxs-lookup"><span data-stu-id="958d4-103">Product lifecycle state</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="958d4-104">Livssyklustilstand for produkter dokumenterer livssyklustilstanden til et frigitt produkt eller produktvariant.</span><span class="sxs-lookup"><span data-stu-id="958d4-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="958d4-105">Produktlivssyklustilstander defineres av brukeren, vanligvis produktsjefen eller ansvarlig for produktstandarddata.</span><span class="sxs-lookup"><span data-stu-id="958d4-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="958d4-106">Bestemte forretningsprosesser, for eksempel hovedplanlegging, kan påvirkes av en bestemt livssyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="958d4-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   
 
<span data-ttu-id="958d4-107">Et frigitt produkt eller produktvariant kan knyttes til en produktlivssyklustilstand som dokumenterer hvilken livssyklustilstand et bestemt produkt eller en variant befinner seg i.</span><span class="sxs-lookup"><span data-stu-id="958d4-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="958d4-108">Du kan definere antall produktlivssyklustilstander ved å tilordne statusnavn og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="958d4-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="958d4-109">Du kan velge én livssyklustilstand som standardinnstilling for nye frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="958d4-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="958d4-110">Frigitte produktvarianter arver produktlivssyklustilstanden fra deres frigitte produktstandard ved oppretting.</span><span class="sxs-lookup"><span data-stu-id="958d4-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="958d4-111">Når du endrer livssyklustilstanden for en frigitt produktstandard, kan du velge å oppdatere alle eksisterende varianter som har samme opprinnelige tilstand.</span><span class="sxs-lookup"><span data-stu-id="958d4-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="958d4-112">Opprette en ny livssyklustilstand for produkt</span><span class="sxs-lookup"><span data-stu-id="958d4-112">Create a new product lifecycle state</span></span> 
 
- <span data-ttu-id="958d4-113">Hvis du vil opprette en ny produktlivssyklustilstand, spiller eller leser du oppgaveveiledningen **Opprette en ny livssyklustilstand for produkt**.</span><span class="sxs-lookup"><span data-stu-id="958d4-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="958d4-114">Hvis du vil opprette en standard produktlivssyklustilstand, spiller eller leser du oppgaveveiledningen **Opprette en standard livssyklustilstand for produkt**.</span><span class="sxs-lookup"><span data-stu-id="958d4-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="958d4-115">Knytte produktlivssyklustilstander til frigitte produkter</span><span class="sxs-lookup"><span data-stu-id="958d4-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="958d4-116">Det finnes flere måter å knytte en produktlivssyklustilstand til frigitte produkter og produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="958d4-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="958d4-117">Ved oppretting av et nytt frigitt produkt tilordnes standard **livssyklustilstand for produkt** automatisk.</span><span class="sxs-lookup"><span data-stu-id="958d4-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="958d4-118">Ved frigivelse av et produkt til en juridisk enhet tilordnes standard **livssyklustilstand for produkt** automatisk.</span><span class="sxs-lookup"><span data-stu-id="958d4-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="958d4-119">Ved frigivelse av en produktvariant til en juridisk enhet tilordnes **livssyklustilstanden for produkt** som er knyttet til den frigitte produktstandarden i denne juridiske enheten, automatisk til den nye varianten.</span><span class="sxs-lookup"><span data-stu-id="958d4-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="958d4-120">Du kan oppdatere produktlivssyklustilstanden manuelt ved hjelp av:</span><span class="sxs-lookup"><span data-stu-id="958d4-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="958d4-121">**Frigitte produkter**-listesiden eller **Detaljvisning**.</span><span class="sxs-lookup"><span data-stu-id="958d4-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="958d4-122">**Frigitte produktvarianter**-listesiden eller **Detaljvisning**.</span><span class="sxs-lookup"><span data-stu-id="958d4-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="958d4-123">Finn utdaterte produkter eller produktvarianter basert på behov og tilknytt en livssyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="958d4-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="958d4-124">Hvis du vil ha mer informasjon om hvordan du tilknytter produktlivssyklustilstander, spiller du av eller leser følgende to oppgaveveiledninger.</span><span class="sxs-lookup"><span data-stu-id="958d4-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="958d4-125">Hvis du vil knytte en produktlivssyklustilstand til en frigitt produktstandard, spiller du av eller leser oppgaveveiledningen **Tilordne en produktlivssyklustilstand til en frigitt produktstandard**.</span><span class="sxs-lookup"><span data-stu-id="958d4-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="958d4-126">Hvis du vil knytte en produktlivssyklustilstand til et frigitt produkt, spiller du av eller leser oppgaveveiledningen **Tilordne en produktlivssyklustilstand til et frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="958d4-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="958d4-127">Påvirkning på hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="958d4-127">Impact on master planning</span></span> 

<span data-ttu-id="958d4-128">Produktlivssyklustilstanden har bare ett kontrollflagg: **Er aktiv for planlegging**.</span><span class="sxs-lookup"><span data-stu-id="958d4-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="958d4-129">Som standard er dette satt til **Ja** for alle opprettede produktlivssyklustilstander, men det kan endres til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="958d4-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="958d4-130">Hvis du angir **Nei**, er de tilknyttede frigitte produktene eller frigitte produktvariantene:</span><span class="sxs-lookup"><span data-stu-id="958d4-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="958d4-131">Utelatt fra hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="958d4-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="958d4-132">Ekskludert fra beregning av stykklistenivå.</span><span class="sxs-lookup"><span data-stu-id="958d4-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="958d4-133">Hvis du vil ha mer informasjon om hvordan du bruker produktlivssyklustilstand for å utelate produkter fra hovedplanlegging og stykklistenivåberegning, spiller du av eller leser oppgaveveiledningen **Opprette en produktlivssyklustilstand for å utelukke produkter fra hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="958d4-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="958d4-134">Av hensyn til ytelsen anbefales det å knytte alle foreldede frigitte produkter eller produktvarianter, spesielt når du arbeider med ikke-gjenbrukbare produktkonfigurasjonsvarianter, til en produktlivssyklustilstand som er deaktivert for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="958d4-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  
 
## <a name="default-migration-import-and-export"></a><span data-ttu-id="958d4-135">Standard overføring, import og eksport</span><span class="sxs-lookup"><span data-stu-id="958d4-135">Default migration, import, and export</span></span> 

<span data-ttu-id="958d4-136">Produktlivssyklustilstandene støttes ikke av dataenheter, og livssyklustilstanden kan ikke settes til variabel tilstand via de frigitte produktdataenhetene.</span><span class="sxs-lookup"><span data-stu-id="958d4-136">The product lifecycle states are not supported by data entities, and the lifecycle state cannot be set to a variable state through the released product data entities.</span></span>

-  <span data-ttu-id="958d4-137">Ved overføring fra tidligere versjoner er livssyklustilstanden for alle produkter og produktvarianter tom.</span><span class="sxs-lookup"><span data-stu-id="958d4-137">On migration from previous releases, the lifecycle state of all products and product variants will be blank.</span></span>  
-  <span data-ttu-id="958d4-138">Når du importerer frigitte produkter gjennom en dataenhet, brukes standard livssyklustilstand ved oppretting.</span><span class="sxs-lookup"><span data-stu-id="958d4-138">When importing released products through a data entity, the default lifecycle state will be applied on creation.</span></span>  
-  <span data-ttu-id="958d4-139">Når du importerer frigitte produktvarianter gjennom en dataenhet, importeres produktlivssyklustilstanden til den frigitte produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="958d4-139">When importing released product variants through a data entity, the product lifecycle state of the released product master will be imported.</span></span>   
 
## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="958d4-140">Finn foreldede produkter og produktvarianter</span><span class="sxs-lookup"><span data-stu-id="958d4-140">Find obsolete products and products variants</span></span> 
 
<span data-ttu-id="958d4-141">Du kan kjøre en simuleringsanalyse for å finne de foreldede frigitte produktene eller produktvariantene og deretter oppdatere produktlivssyklusstatusen deres.</span><span class="sxs-lookup"><span data-stu-id="958d4-141">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="958d4-142">Hvis du vil finne utdaterte produkter, kan du spille av eller lese oppgaveveiledningen **Finne utdaterte produktvarianter og tilordne en produktlivssyklustilstand**.</span><span class="sxs-lookup"><span data-stu-id="958d4-142">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="958d4-143">Denne oppgaveveiledningen viser hvordan du finner foreldede frigitte produkter og produktvarianter og hvordan du knytter en produktlivssyklustilstand til de foreldede produktene.</span><span class="sxs-lookup"><span data-stu-id="958d4-143">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="958d4-144">Den viser også hvordan du viser simuleringsresultatene og vurderer hvor mange produkter og produktvarianter som skal være tilknyttet en ny produktlivssyklustilstand når du kjører oppdateringen uten simulering.</span><span class="sxs-lookup"><span data-stu-id="958d4-144">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  
 
<span data-ttu-id="958d4-145">Ved å kjøre analysen i simuleringsmodus vises produktene og produktvariantene som er identifisert som foreldede, i et bestemt skjema, der de kan lett kan gjennomgås.</span><span class="sxs-lookup"><span data-stu-id="958d4-145">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="958d4-146">Analysen søker etter transaksjoner og bestemte hoveddata for å identifisere produkter som ikke har etterspørsel i en variabel periode, og ingen hoveddata som kan føre til etterspørsel.</span><span class="sxs-lookup"><span data-stu-id="958d4-146">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="958d4-147">Ny frigitte produkter i en variabel periode kan utelates fra analysen.</span><span class="sxs-lookup"><span data-stu-id="958d4-147">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="958d4-148">Når analysesimuleringen returnerer det forventede resultatet, kan brukeren kjøre analysen og angi en ny produktlivssyklustilstand for alle produkter som er identifisert som foreldede i analysen.</span><span class="sxs-lookup"><span data-stu-id="958d4-148">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  
 
> [!NOTE]
> <span data-ttu-id="958d4-149">Vær oppmerksom på at alle analyser og oppdateringer må gjøres innenfor samme juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="958d4-149">Note that all analysis and updates must be done within the same legal entity.</span></span>  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="958d4-150">Kriterier for å velge og oppdatere frigitte produkter og produktvarianter</span><span class="sxs-lookup"><span data-stu-id="958d4-150">Criteria to select and update released products or product variants</span></span> 
 
<span data-ttu-id="958d4-151">Bruk følgende kriterier for å velge og oppdatere de frigitte produktene og produktvariantene:</span><span class="sxs-lookup"><span data-stu-id="958d4-151">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="958d4-152">Produktlivssyklustilstanden for produktet eller produktvarianten må være forskjellig fra den nye ønskede tilstanden.</span><span class="sxs-lookup"><span data-stu-id="958d4-152">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="958d4-153">Produktet eller produktvarianten ble opprettet for noen dager siden basert på antallet dager du angir i dialogboksen for valg.</span><span class="sxs-lookup"><span data-stu-id="958d4-153">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="958d4-154">Det finnes ingen åpne produksjonsordrer (= status < avsluttet) for produktet eller produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="958d4-154">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="958d4-155">Det finnes ingen åpne lagertransaksjoner (= status problem ReservPhysical til QuotationIssue eller status mottak Registrered til QuotationReceipt) for produktet eller produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="958d4-155">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="958d4-156">Det finnes ingen lagertransaksjoner i løpet av de siste antall dagene for produktet eller produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="958d4-156">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="958d4-157">Det finnes ikke noe fremtidig behov eller forsyningsprognose for produktet eller produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="958d4-157">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="958d4-158">Minimumsnivå for lager er ikke angitt i varedekning for produktet eller produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="958d4-158">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="958d4-159">Ingen aktiv kanban-regel for fast antall for produktet eller produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="958d4-159">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="958d4-160">Ingen serviceordrelinje for produktet eller produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="958d4-160">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="958d4-161">Ingen aktive eller fremtidige salgs- eller kjøpsavtalelinjer for produktet eller produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="958d4-161">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="958d4-162">Produktet eller produktvarianten brukes ikke i en stykkliste som er knyttet til en ikke-utløpt godkjent stykklisteversjon for et produkt eller en variant som er aktivert for planlegging.</span><span class="sxs-lookup"><span data-stu-id="958d4-162">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="958d4-163">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="958d4-163">Related topics</span></span>

-  <span data-ttu-id="958d4-164">Opprette en ny livssyklustilstand for produkt</span><span class="sxs-lookup"><span data-stu-id="958d4-164">Create a new product lifecycle state</span></span>
-  <span data-ttu-id="958d4-165">Opprette en standard ny livssyklustilstand for produkt</span><span class="sxs-lookup"><span data-stu-id="958d4-165">Create a default new product lifecycle state</span></span>
-  <span data-ttu-id="958d4-166">Tilordne en produktlivssyklustilstand til en frigitt produktstandard</span><span class="sxs-lookup"><span data-stu-id="958d4-166">Assign a product lifecycle state to a released product master</span></span>
-  <span data-ttu-id="958d4-167">Tilordne en produktlivssyklustilstand til et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="958d4-167">Assign a product lifecycle state to a released product</span></span>
-  <span data-ttu-id="958d4-168">inne utdaterte produktvarianter og tilordne en produktlivssyklustilstand</span><span class="sxs-lookup"><span data-stu-id="958d4-168">Find obsolete product variants and assign a product lifecycle state</span></span>
-  <span data-ttu-id="958d4-169">Opprette en produktlivssyklustilstand for å utelukke produkter fra hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="958d4-169">Create a product lifecycle state to exclude products from Master planning</span></span>

