---
title: Behandling av skift og kassaskuff
description: Dette emnet beskriver hvordan du definerer og bruker skift på salgssteder i Commerce.
author: jblucher
manager: AnnBe
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 32b7be42509a2c857f1357eb64a6b488f9cd2269
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023559"
---
# <a name="shift-and-cash-drawer-management"></a><span data-ttu-id="652ca-103">Behandling av skift og kassaskuff</span><span class="sxs-lookup"><span data-stu-id="652ca-103">Shift and cash drawer management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="652ca-104">Dette emnet beskriver hvordan du definerer og bruker skift på salgssteder i Commerce.</span><span class="sxs-lookup"><span data-stu-id="652ca-104">This topic explains how to set up and use shifts in Commerce point of sale (POS).</span></span>

<span data-ttu-id="652ca-105">I Dynamics 365 Commerce beskriver *skift* samlingen av transaksjonsdata og aktiviteter mellom to punkter i tid for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="652ca-105">In Dynamics 365 Commerce, the term *shift* describes the collection of POS transactional data and activities between two points in time.</span></span> <span data-ttu-id="652ca-106">For hvert skift sammenlignes forventet beløp sammenlignet med beløpet som ble talt og deklarert.</span><span class="sxs-lookup"><span data-stu-id="652ca-106">For each shift, the amount of money that is expected is compared against the amount that was counted and declared.</span></span>

<span data-ttu-id="652ca-107">Skift åpnes vanligvis i begynnelsen av arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="652ca-107">Typically, shifts are opened at the start of the business day.</span></span> <span data-ttu-id="652ca-108">På dette tidspunktet deklarerer brukeren startbeløpet som kassaskuffen inneholder.</span><span class="sxs-lookup"><span data-stu-id="652ca-108">At that point, a user declares the starting amount that the cash drawer contains.</span></span> <span data-ttu-id="652ca-109">Salgstransaksjoner blir deretter utført i løpet av dagen.</span><span class="sxs-lookup"><span data-stu-id="652ca-109">Sales transactions are then performed throughout the day.</span></span> <span data-ttu-id="652ca-110">På slutten av dagen telles kassaskuffen, og sluttbeløpet deklareres.</span><span class="sxs-lookup"><span data-stu-id="652ca-110">Finally, at the end of the day, the drawer is counted, and the closing amounts are declared.</span></span> <span data-ttu-id="652ca-111">Skiftet lukkes, og det genereres en Z-rapport.</span><span class="sxs-lookup"><span data-stu-id="652ca-111">The shift is closed, and a Z report is generated.</span></span> <span data-ttu-id="652ca-112">Z-rapporten angir om det er for mye eller for lite.</span><span class="sxs-lookup"><span data-stu-id="652ca-112">The Z report indicates whether there is an overage or shortage.</span></span>

## <a name="typical-shift-scenarios"></a><span data-ttu-id="652ca-113">Vanlige skiftet scenarier</span><span class="sxs-lookup"><span data-stu-id="652ca-113">Typical shift scenarios</span></span>

<span data-ttu-id="652ca-114">Commerce gir flere konfigurasjonsalternativer og salgsstedsoperasjoner for å støtte et bredt spekter av forretningsprosesser på slutten av dagen for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="652ca-114">Commerce provides several configuration options and POS operations to support a wide range of end-of-day business processes for the POS.</span></span> <span data-ttu-id="652ca-115">Denne delen beskriver noen vanlige skiftscenarier.</span><span class="sxs-lookup"><span data-stu-id="652ca-115">This section describes some typical shift scenarios.</span></span>

### <a name="fixed-till"></a><span data-ttu-id="652ca-116">Fast kasse</span><span class="sxs-lookup"><span data-stu-id="652ca-116">Fixed till</span></span>

<span data-ttu-id="652ca-117">Dette er vanligvis brukt oftest.</span><span class="sxs-lookup"><span data-stu-id="652ca-117">Traditionally, this scenario has been used most often.</span></span> <span data-ttu-id="652ca-118">Det brukes forsatt mye.</span><span class="sxs-lookup"><span data-stu-id="652ca-118">It's still extensively used.</span></span> <span data-ttu-id="652ca-119">I et "fast kasse"-skift tilknyttes skiftet og kassen med en bestemt kasse.</span><span class="sxs-lookup"><span data-stu-id="652ca-119">In a "fixed till" shift, the shift and till are associated with a specific register.</span></span> <span data-ttu-id="652ca-120">De flyttes fra én kasse til en annen.</span><span class="sxs-lookup"><span data-stu-id="652ca-120">They aren't moved from one register to another.</span></span> <span data-ttu-id="652ca-121">Et "fast kasse"-skift kan brukes av én bruker eller deles mellom flere brukere.</span><span class="sxs-lookup"><span data-stu-id="652ca-121">A "fixed till" shift can be used by a single user or shared among multiple users.</span></span> <span data-ttu-id="652ca-122">"Fast kasse"-skift krever ikke noen spesiell konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="652ca-122">"Fixed till" shifts don't require any special configuration.</span></span>

### <a name="floating-till"></a><span data-ttu-id="652ca-123">Flytende kasse</span><span class="sxs-lookup"><span data-stu-id="652ca-123">Floating till</span></span>

<span data-ttu-id="652ca-124">I et "flytende kasse"-skift kan skiftet og kassen flyttes fra én kasse til en annen.</span><span class="sxs-lookup"><span data-stu-id="652ca-124">In a "floating till" shift, the shift and cash drawer can be moved from one register to another.</span></span> <span data-ttu-id="652ca-125">Selv om en kasse bare kan ha ett aktivt skift per kasse, kan skift stoppes og startes opp igjen senere eller på en annen kasse.</span><span class="sxs-lookup"><span data-stu-id="652ca-125">Although a register can have only one active shift per cash drawer, shifts can be suspended and then resumed later or on a different register.</span></span>

<span data-ttu-id="652ca-126">En butikk har for eksempel to kasser.</span><span class="sxs-lookup"><span data-stu-id="652ca-126">For example, a store has two registers.</span></span> <span data-ttu-id="652ca-127">Hver kasse åpnes ved starten av dagen når kassereren åpner et nytt skift og angir startbeløpet.</span><span class="sxs-lookup"><span data-stu-id="652ca-127">Each register is opened at the start of the day when the cashier opens a new shift and provides the starting amount.</span></span> <span data-ttu-id="652ca-128">Når én kasserer er klar til å ta en pause, stopper kassereren hans eller hennes skift og kassen og fjerner kassen fra kassaskuffen.</span><span class="sxs-lookup"><span data-stu-id="652ca-128">When one cashier is ready to take a break, that cashier suspends his or her shift and removes the till from the cash drawer.</span></span> <span data-ttu-id="652ca-129">Denne kassen blir da tilgjengelig for andre kasserere.</span><span class="sxs-lookup"><span data-stu-id="652ca-129">That register then becomes available to other cashiers.</span></span> <span data-ttu-id="652ca-130">En annen kasserer kan logge på og åpne sitt eget skift på kassen.</span><span class="sxs-lookup"><span data-stu-id="652ca-130">Another cashier can sign in to and open his or her own shift on the register.</span></span> <span data-ttu-id="652ca-131">Etter at den pausen til den første kassereren er avsluttet, kan denne kassereren gjenoppta hans eller hennes skift når en av de andre kassene blir tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="652ca-131">After the first cashier's break has ended, that cashier can resume his or her shift when one of the other registers becomes available.</span></span> <span data-ttu-id="652ca-132">"Flytense kasse"-skift krever ikke noen spesiell konfigurasjon eller tillatelse.</span><span class="sxs-lookup"><span data-stu-id="652ca-132">"Floating till" shifts don't require any special configuration or permission.</span></span>

### <a name="single-user"></a><span data-ttu-id="652ca-133">Enkeltbruker</span><span class="sxs-lookup"><span data-stu-id="652ca-133">Single user</span></span>

<span data-ttu-id="652ca-134">Mange forhandlere foretrekker å tillate bare én bruker pers skift for å garantere det høyeste nivået av ansvar for kontanter i kassaskuffen.</span><span class="sxs-lookup"><span data-stu-id="652ca-134">Many retailers prefer to allow only one user per shift, to help guarantee the highest level of accountability for the cash in the cash drawer.</span></span> <span data-ttu-id="652ca-135">Hvis bare én bruker har tilgang til å bruke kassen som er knyttet til et skift, vil denne brukeren ene og alene holdes ansvarlig for eventuelle avvik.</span><span class="sxs-lookup"><span data-stu-id="652ca-135">If only one user is allowed to use the till that is associated with a shift, that user can be held solely responsible for any discrepancies.</span></span> <span data-ttu-id="652ca-136">Hvis flere brukere bruker et skift, er det vanskelig å avgjøre hvem som har gjort en feil eller som kanskje prøver å stjele fra kassen.</span><span class="sxs-lookup"><span data-stu-id="652ca-136">If more than one user uses a shift, it's difficult to determine who made an error, or who might be trying to steal from the till.</span></span>

### <a name="multiple-users"></a><span data-ttu-id="652ca-137">Flere brukere</span><span class="sxs-lookup"><span data-stu-id="652ca-137">Multiple users</span></span>

<span data-ttu-id="652ca-138">Noen forhandlerne er villige til å ofre ansvarsnivået son enkeltbrukerskift gir, og tillate flere brukere per skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-138">Some retailers are willing to sacrifice the level of accountability that single-user shifts provide and to allow more than one user per shift.</span></span> <span data-ttu-id="652ca-139">Dette er vanlig når det er flere brukere enn tilgjengelige kasser, og behovet for fleksibilitet og hastighet oppveier muligheten for tap.</span><span class="sxs-lookup"><span data-stu-id="652ca-139">This approach is typical when there are more users than available registers, and the need for flexibility and speed outweighs the potential for loss.</span></span> <span data-ttu-id="652ca-140">Det er også vanlig når butikksjefer ikke har sine egne skift, men etter behov kan bruke et skift for en av kassererne.</span><span class="sxs-lookup"><span data-stu-id="652ca-140">It's also typical when store managers don't have their own shifts but can, as required, use the shifts of any of their cashiers.</span></span> <span data-ttu-id="652ca-141">For å logge på og bruke et skift som ble åpnet av en annen bruker, må en bruker ha salgsstedstillatelsen **Tillat pålogging av flere skift**.</span><span class="sxs-lookup"><span data-stu-id="652ca-141">To sign in to and use a shift that was opened by another user, a user must have the **Allow multiple shift logon** POS permission.</span></span>

### <a name="shared-shift"></a><span data-ttu-id="652ca-142">Delte skift</span><span class="sxs-lookup"><span data-stu-id="652ca-142">Shared shift</span></span>

<span data-ttu-id="652ca-143">En "delt skift"-konfigurasjon lar forhandlere ha ett enkelt skift på tvers av flere kasser, pengeskuffer og brukere.</span><span class="sxs-lookup"><span data-stu-id="652ca-143">A "shared shift" configuration lets retailers have a single shift across multiple registers, cash drawers, and users.</span></span> <span data-ttu-id="652ca-144">Et delt skift har ett enkelt startbeløp og ett enkelt sluttbeløp som summeres på tvers av alle kassaskuffer.</span><span class="sxs-lookup"><span data-stu-id="652ca-144">A shared shift has a single starting amount and a single closing amount that are summarized across all cash drawers.</span></span> <span data-ttu-id="652ca-145">Delte skift er vanligst når mobilenheter brukes.</span><span class="sxs-lookup"><span data-stu-id="652ca-145">Shared shifts are most typical when mobile devices are used.</span></span> <span data-ttu-id="652ca-146">I så fall er ikke en kassaskuff reservert for hver kasse.</span><span class="sxs-lookup"><span data-stu-id="652ca-146">In this scenario, a separate cash drawer isn't reserved for each register.</span></span> <span data-ttu-id="652ca-147">I stedet kan alle kasser dele én kassaskuff.</span><span class="sxs-lookup"><span data-stu-id="652ca-147">Instead, all registers can share one cash drawer.</span></span>

<span data-ttu-id="652ca-148">For delte skift som skal brukes i en butikk må kassaskuffen konfigureres som en "kassakuff for delt skift" på **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Maskinvareprofiler \> Skuff**.</span><span class="sxs-lookup"><span data-stu-id="652ca-148">For shared shifts to be used in a store, the cash drawer must be configured as a "shared shift drawer" at **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles \> Drawer**.</span></span> <span data-ttu-id="652ca-149">Brukerne må i tillegg ha ett eller begge av de delte skifttillatelsene (Tillat administrasjon av delte skift og Tillat bruk av delt skift).</span><span class="sxs-lookup"><span data-stu-id="652ca-149">Additionally, users must have one or both of the shared shift permissions (Allow manage shared shift and Allow use shared shift).</span></span>

> [!NOTE]
> <span data-ttu-id="652ca-150">Bare ett delt skift kan være åpent om gangen i hver butikk.</span><span class="sxs-lookup"><span data-stu-id="652ca-150">Only one shared shift can be open at a time in each store.</span></span> <span data-ttu-id="652ca-151">Delte skift og frittstående skift kan brukes i den samme butikken.</span><span class="sxs-lookup"><span data-stu-id="652ca-151">Shared shifts and stand-alone shifts can be used in the same store.</span></span>

## <a name="shift-and-drawer-operations"></a><span data-ttu-id="652ca-152">Skift og skuffoperasjoner</span><span class="sxs-lookup"><span data-stu-id="652ca-152">Shift and drawer operations</span></span>

<span data-ttu-id="652ca-153">Forskjellige operasjoner kan utføres for å endre statusen for et skift, eller for å øke eller redusere pengebeløpet i kassaskuffen.</span><span class="sxs-lookup"><span data-stu-id="652ca-153">Various operations can be performed to change the state of a shift, or to increase or decrease the amount of money in the cash drawer.</span></span> <span data-ttu-id="652ca-154">Dette avsnittet beskriver disse skiftoperasjonene for Modern POS og Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="652ca-154">This section describes these shift operations for Modern POS and Cloud POS.</span></span>

### <a name="open-shift"></a><span data-ttu-id="652ca-155">Åpne skift</span><span class="sxs-lookup"><span data-stu-id="652ca-155">Open shift</span></span>

<span data-ttu-id="652ca-156">Salgsstedet krever at brukere har et aktivt, åpent skift for å utføre handlinger som vil resultere i en finanstransaksjon, for eksempel salg, retur eller kundeordre.</span><span class="sxs-lookup"><span data-stu-id="652ca-156">The POS requires that users have an active, open shift in order to perform any operations that will produce a financial transaction, such as a sale, return, or customer order.</span></span>

<span data-ttu-id="652ca-157">Når en bruker logger på salgsstedet, vil systemet først kontrollerer om et aktivt skift er tilgjengelig for denne brukeren på den aktuelle kassen.</span><span class="sxs-lookup"><span data-stu-id="652ca-157">When a user signs in to the POS, the system first verifies whether an active shift is available for that user on the current register.</span></span> <span data-ttu-id="652ca-158">Hvis et aktivt skift ikke er tilgjengelig, kan brukeren åpne et nytt skift, gjenoppta et eksisterende skift eller fortsette å logge på i "ikke-skuff"-modus, avhengig av systemkonfigurasjonen og brukerens tillatelser.</span><span class="sxs-lookup"><span data-stu-id="652ca-158">If an active shift isn't available, the user can open a new shift, resume an existing shift, or sign in in "non-drawer" mode, depending on the system configuration and the user's permissions.</span></span>

### <a name="declare-start-amount"></a><span data-ttu-id="652ca-159">Rapporter startbeløp</span><span class="sxs-lookup"><span data-stu-id="652ca-159">Declare start amount</span></span>

<span data-ttu-id="652ca-160">Denne operasjonen er ofte den første operasjonen som utføres et nylig åpnet skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-160">This operation is often the first operation that is performed for a newly opened shift.</span></span> <span data-ttu-id="652ca-161">For denne operasjonen angir brukere startbeløpet i kassaskuffen for skiftet.</span><span class="sxs-lookup"><span data-stu-id="652ca-161">For this operation, users specify the starting cash amount in the cash drawer for the shift.</span></span> <span data-ttu-id="652ca-162">Denne operasjonen er viktig på grunn av beregningen av for mye/lite som utføres når et skift som lukkes vurderer startbeløpet.</span><span class="sxs-lookup"><span data-stu-id="652ca-162">This operation is important because the overage/shortage calculation that occurs when a shift is closed considers the start amount.</span></span>

### <a name="float-entry"></a><span data-ttu-id="652ca-163">Flytoppføring</span><span class="sxs-lookup"><span data-stu-id="652ca-163">Float entry</span></span>

<span data-ttu-id="652ca-164">*Flytoppføringer* er ikke-salgstransaksjoner som utføres i et aktivt skift for å øke pengebeløpet i kassaskuffen.</span><span class="sxs-lookup"><span data-stu-id="652ca-164">*Float entries* are non-sales transactions that are performed in an active shift to increase the amount of cash in the cash drawer.</span></span> <span data-ttu-id="652ca-165">Et vanlig eksempel på en flytoppføring er å legge til flere vekslepenger i skuffen når det er lite.</span><span class="sxs-lookup"><span data-stu-id="652ca-165">A typical example of a float entry is a transaction to add additional change to the drawer when it's running low.</span></span>

### <a name="tender-removal"></a><span data-ttu-id="652ca-166">Fjerning av betalingsmidler</span><span class="sxs-lookup"><span data-stu-id="652ca-166">Tender removal</span></span>

<span data-ttu-id="652ca-167">*Fjerning av betalingsmidler* er ikke-salgstransaksjoner som utføres i et aktivt skift for å redusere pengebeløpet i kassaskuffen.</span><span class="sxs-lookup"><span data-stu-id="652ca-167">*Tender removals* are non-sales transactions that are performed in an active shift to reduce the amount of cash in the cash drawer.</span></span> <span data-ttu-id="652ca-168">Denne operasjonen brukes vanligvis sammen med en flytoppføringsoperasjon i et annet skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-168">This operation is most often used in conjunction with a Float entry operation on a different shift.</span></span> <span data-ttu-id="652ca-169">Kasse 1 har for eksempel lite vekslepenger, så brukeren på kasse 2 utfører en fjerning av betalingsmidler for å redusere beløpet i kassaskuffen.</span><span class="sxs-lookup"><span data-stu-id="652ca-169">For example, because register 1 is running low on change, the user on register 2 does a tender removal to reduce the amount in his or her cash drawer.</span></span> <span data-ttu-id="652ca-170">Brukeren i kasse 1 gjør deretter en flytoppføring for å øke beløpet i hans eller hennes kassaskuff.</span><span class="sxs-lookup"><span data-stu-id="652ca-170">The user on register 1 then does a float entry to increase the amount in his or her cash drawer.</span></span>

### <a name="suspend-shift"></a><span data-ttu-id="652ca-171">Avbryt skift</span><span class="sxs-lookup"><span data-stu-id="652ca-171">Suspend shift</span></span>

<span data-ttu-id="652ca-172">Brukere kan deaktivere sine aktive skift for å frigjøre gjeldende kasse for en annen bruker, eller flytte skiftet til en annen kasse (dette er kalles skiftet ofte et "flytende kasse"-skift).</span><span class="sxs-lookup"><span data-stu-id="652ca-172">Users can suspend their active shift to free up the current register for another user, or to move their shift to a different register (in this case, the shift is often referred to as a "floating till" shift).</span></span>

<span data-ttu-id="652ca-173">Suspendering av skiftet forhindrer eventuelle nye transaksjoner eller endringer til skiftet før det gjenopptas.</span><span class="sxs-lookup"><span data-stu-id="652ca-173">Suspension of a shift prevents any new transactions or changes to the shift until it's resumed.</span></span>

### <a name="resume-shift"></a><span data-ttu-id="652ca-174">Gjenoppta skift</span><span class="sxs-lookup"><span data-stu-id="652ca-174">Resume shift</span></span>

<span data-ttu-id="652ca-175">Denne operasjonen lar bruker gjenoppta et tidligere suspendert skift i en kasse som ikke allerede har et aktivt skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-175">This operation lets users resume a previously suspended shift on any register that doesn't already have an active shift.</span></span>

### <a name="tender-declaration"></a><span data-ttu-id="652ca-176">Kasseoppgjør</span><span class="sxs-lookup"><span data-stu-id="652ca-176">Tender declaration</span></span>

<span data-ttu-id="652ca-177">Denne operasjonen utføres for å angi det totale beløpet som er i kassaskuffen.</span><span class="sxs-lookup"><span data-stu-id="652ca-177">This operation is performed to specify the total amount of money that is currently in the cash drawer.</span></span> <span data-ttu-id="652ca-178">Brukere utføre oftest operasjonen før de lukker et skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-178">Users most often perform this operation before they close a shift.</span></span> <span data-ttu-id="652ca-179">Det angitte beløpet sammenlignes med det forventede skiftbeløpet for å beregne over-/underbeløpet.</span><span class="sxs-lookup"><span data-stu-id="652ca-179">The specified amount is compared against the expected shift amount to calculate the overage/shortage amount.</span></span>

### <a name="safe-drop"></a><span data-ttu-id="652ca-180">Deponer til safe</span><span class="sxs-lookup"><span data-stu-id="652ca-180">Safe drop</span></span>

<span data-ttu-id="652ca-181">Deponeringer til safe kan når som helst utføres på et aktivt skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-181">Safe drops can be done on an active shift at any time.</span></span> <span data-ttu-id="652ca-182">Denne operasjonen fjerner penger fra kassaskuffen, slik at de kan overføres til en sikrere plassering, så som en safe på bakrommet.</span><span class="sxs-lookup"><span data-stu-id="652ca-182">This operation removes money from the cash drawer so that it can be transferred to a more secure location, such as a safe in the back room.</span></span> <span data-ttu-id="652ca-183">Det totale beløpet som er registrert for deponeringer til safe, er fremdeles inkludert i skifttotalene, men trenger ikke regnes som en del av kasseoppgjøret.</span><span class="sxs-lookup"><span data-stu-id="652ca-183">The total amount that is recorded for safe drops is included in shift totals, but it doesn't have to be counted as part of the tender declaration.</span></span>

### <a name="bank-drop"></a><span data-ttu-id="652ca-184">Deponer til bank</span><span class="sxs-lookup"><span data-stu-id="652ca-184">Bank drop</span></span>

<span data-ttu-id="652ca-185">I likhet med deponeringer til safe utføres også deponeringer til bank på aktive skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-185">Like safe drops, bank drops are done on active shifts.</span></span> <span data-ttu-id="652ca-186">Denne operasjonen fjerner penger fra skiftet for å klargjøre for bankinnskuddet.</span><span class="sxs-lookup"><span data-stu-id="652ca-186">This operation removes money from the shift to prepare for the bank deposit.</span></span>

### <a name="blind-close-shift"></a><span data-ttu-id="652ca-187">Lukk skift usporet</span><span class="sxs-lookup"><span data-stu-id="652ca-187">Blind close shift</span></span>

<span data-ttu-id="652ca-188">*Lukkede usporede skift* er ikke lenger er aktive, men er ikke fullstendig lukket.</span><span class="sxs-lookup"><span data-stu-id="652ca-188">*Blind-closed shifts* are no longer active but haven't been fully closed.</span></span> <span data-ttu-id="652ca-189">I motsetning til skift kan ikke lukkede usporede skift gjenopptas.</span><span class="sxs-lookup"><span data-stu-id="652ca-189">Unlike suspended shifts, blind-closed shifts can't be resumed.</span></span> <span data-ttu-id="652ca-190">Operasjoner, for eksempel Rapporter startbeløp og Kasseoppgjør, kan imidlertid utføres på dem senere eller fra en annen kasse.</span><span class="sxs-lookup"><span data-stu-id="652ca-190">However, operations such as Declare start amount and Tender declaration can be performed on them later or from a different register.</span></span>

<span data-ttu-id="652ca-191">Lukkede usporede skift brukes ofte til å frigjøre et register for en ny bruker eller skift, uten først å telle, avstemme og lukke dette skiftet fullstendig.</span><span class="sxs-lookup"><span data-stu-id="652ca-191">Blind-closed shifts are often used to free up a register for a new user or shift without first having to fully count, reconcile, and close the shift.</span></span>

### <a name="close-shift"></a><span data-ttu-id="652ca-192">Lukk skift</span><span class="sxs-lookup"><span data-stu-id="652ca-192">Close shift</span></span>

<span data-ttu-id="652ca-193">Denne operasjonen beregner totaler for skift og over-/underbeløp, og fullfører deretter et aktivt eller lukket usporet skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-193">This operation calculates shift totals and overage/shortage amounts, and then finalizes an active or blind-closed shift.</span></span> <span data-ttu-id="652ca-194">Avhengig av brukerens tillatelser skrives også en Z-rapport for skiftet.</span><span class="sxs-lookup"><span data-stu-id="652ca-194">Depending on the user's permissions, a Z report is also printed for the shift.</span></span> <span data-ttu-id="652ca-195">Lukkede skift kan ikke gjenopptas eller endres.</span><span class="sxs-lookup"><span data-stu-id="652ca-195">Closed shifts can't be resumed or modified.</span></span>

### <a name="print-x"></a><span data-ttu-id="652ca-196">Skriv ut X</span><span class="sxs-lookup"><span data-stu-id="652ca-196">Print X</span></span>

<span data-ttu-id="652ca-197">Denne operasjonen genererer og skriver ut en X-rapport for gjeldende aktive skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-197">This operation generates and prints an X report for the current active shift.</span></span>

### <a name="reprint-z"></a><span data-ttu-id="652ca-198">Skriv ut Z på nytt</span><span class="sxs-lookup"><span data-stu-id="652ca-198">Reprint Z</span></span>

<span data-ttu-id="652ca-199">Denne operasjonen skriver ut den siste Z-rapporten på nytt som blir generert da et skift ble lukket.</span><span class="sxs-lookup"><span data-stu-id="652ca-199">This operation reprints the last Z report that the system generated when a shift was closed.</span></span>

### <a name="manage-shifts"></a><span data-ttu-id="652ca-200">Behandle skift</span><span class="sxs-lookup"><span data-stu-id="652ca-200">Manage shifts</span></span>

<span data-ttu-id="652ca-201">Denne operasjonen lar brukerne vise alle aktive, suspenderte og lukkede usporede skift for butikken.</span><span class="sxs-lookup"><span data-stu-id="652ca-201">This operation lets users view all active, suspended, and blind-closed shifts for the store.</span></span> <span data-ttu-id="652ca-202">Avhengig av tillatelsene kan brukere utføre sine endelige lukkingsprosedyrer, for eksempel Kasseoppgjør og Lukk skift for lukkede usporede skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-202">Depending on their permissions, users can perform their final closing procedures, such as Tender declaration and Close shift operations for blind-closed shifts.</span></span> <span data-ttu-id="652ca-203">Denne operasjonen lar også brukere vise og slette ugyldige skift hvis et skift står i en ugyldig tilstand etter å ha byttet mellom frakoblet og tilkoblet modus.</span><span class="sxs-lookup"><span data-stu-id="652ca-203">This operation also lets users view and delete invalid shifts, in the rare event that shifts are left in a bad state after a switch between offline and online modes.</span></span> <span data-ttu-id="652ca-204">Disse ugyldige skiftene inneholder ingen økonomisk informasjon eller transaksjonsdata som trengs for avstemming.</span><span class="sxs-lookup"><span data-stu-id="652ca-204">These invalid shifts don't contain any financial information or transactional data that is required for reconciliation.</span></span>

## <a name="shift-and-drawer-permissions"></a><span data-ttu-id="652ca-205">Skift og skufftillatelser</span><span class="sxs-lookup"><span data-stu-id="652ca-205">Shift and drawer permissions</span></span>

<span data-ttu-id="652ca-206">Følgende salgsstedstillatelser påvirker hva en bruker kan og ikke kan gjøre i ulike scenarier:</span><span class="sxs-lookup"><span data-stu-id="652ca-206">The following POS permissions affect what a user can and can't do in various scenarios:</span></span>

- <span data-ttu-id="652ca-207">**Tillat usporet lukking**</span><span class="sxs-lookup"><span data-stu-id="652ca-207">**Allow blind close**</span></span>
- <span data-ttu-id="652ca-208">**Tillat utskrift av X-rapport**</span><span class="sxs-lookup"><span data-stu-id="652ca-208">**Allow X-report printing**</span></span>
- <span data-ttu-id="652ca-209">**Tillat utskrift av Z-rapport**</span><span class="sxs-lookup"><span data-stu-id="652ca-209">**Allow Z-report printing**</span></span>
- <span data-ttu-id="652ca-210">**Tillat kasseoppgjør**</span><span class="sxs-lookup"><span data-stu-id="652ca-210">**Allow tender declaration**</span></span>
- <span data-ttu-id="652ca-211">**Tillat flytende rapportering**</span><span class="sxs-lookup"><span data-stu-id="652ca-211">**Allow floating declaration**</span></span>
- <span data-ttu-id="652ca-212">**Åpne skuff uten salg**</span><span class="sxs-lookup"><span data-stu-id="652ca-212">**Open drawer without sale**</span></span>
- <span data-ttu-id="652ca-213">**Tillat pålogging av flere skift** – Denne tillatelsen lar brukere logge på og bruke et skift som en annen bruker åpnet.</span><span class="sxs-lookup"><span data-stu-id="652ca-213">**Allow multiple shift logon** – This permission allows the user to sign in to and use a shift that a different user opened.</span></span> <span data-ttu-id="652ca-214">Brukere som ikke har denne tillatelsen kan bare logge på og bruke skift som vedkommende har åpnet.</span><span class="sxs-lookup"><span data-stu-id="652ca-214">Users who don't have this permission can sign in to and use only shifts that they have opened.</span></span>
- <span data-ttu-id="652ca-215">**Tillat administrasjon av delte skift** – Brukere må ha denne tillatelse for å åpne eller lukke et delt skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-215">**Allow manage shared shift** – Users must have this permission to open or close a shared shift.</span></span>
- <span data-ttu-id="652ca-216">**Tillat bruk av delte skift** – Brukere må ha denne tillatelse for å logge på og bruke et delt skift.</span><span class="sxs-lookup"><span data-stu-id="652ca-216">**Allow use shared shift** – Users must have this permission to sign in to and use a shared shift.</span></span>

## <a name="back-office-end-of-day-considerations"></a><span data-ttu-id="652ca-217">Hensyn å ta ved Back Office-dagsoppgjør</span><span class="sxs-lookup"><span data-stu-id="652ca-217">Back-office end-of-day considerations</span></span>

<span data-ttu-id="652ca-218">Måten skift og kontantskuffavstemming brukes på salgsstedet er forskjellig fra måten at transaksjonsdata summers under utdragsberegning.</span><span class="sxs-lookup"><span data-stu-id="652ca-218">The way that shifts and cash drawer reconciliation are used in the POS differs from the way that transaction data is summarized during statement calculation.</span></span> <span data-ttu-id="652ca-219">Det er viktig at du forstår denne forskjellen.</span><span class="sxs-lookup"><span data-stu-id="652ca-219">It's important that you understand this difference.</span></span> <span data-ttu-id="652ca-220">Avhengig av konfigurasjon og forretningsprosesser kan skiftdataene på salgsstedet (Z-rapporten) og et beregnede utdrag i Back Office gi deg forskjellige resultater.</span><span class="sxs-lookup"><span data-stu-id="652ca-220">Depending on your configuration and your business processes, the shift data in the POS (the Z report) and a calculated statement in the back office can give you different results.</span></span> <span data-ttu-id="652ca-221">Denne forskjellen betyr ikke nødvendigvis at skiftdataene eller det beregnede utdraget er feil, eller at det er et problem med dataene.</span><span class="sxs-lookup"><span data-stu-id="652ca-221">This difference doesn't necessarily mean that either the shift data or the calculated statement is incorrect, or that there is a problem with the data.</span></span> <span data-ttu-id="652ca-222">Det betyr at bare at de angitte parameterne kan inneholde tilleggstransaksjoner eller færre transaksjoner, eller at transaksjonene har blitt summert på forskjellige måter.</span><span class="sxs-lookup"><span data-stu-id="652ca-222">It just means that the parameters that are provided might be including additional transaction or fewer transactions, or that the transactions have been summarized differently.</span></span>

<span data-ttu-id="652ca-223">Selv om alle forhandleren har ulike forretningsbehov, anbefaler vi at du stiller inn systemet på følgende måte for å unngå situasjoner der forskjeller av denne typen oppstår:</span><span class="sxs-lookup"><span data-stu-id="652ca-223">Although every retailer has different business requirements, we recommend that you set up your system in the following way to avoid situations where differences of this type occur:</span></span>

<span data-ttu-id="652ca-224">Gå til **Retail og Commerce \> Kanaler \> Butikker \> Alle butikker \> Utdrag/avslutning**, og for hver butikk setter du feltet **Utdragsmetode** og **Avslutningsmetode** til **Skift**.</span><span class="sxs-lookup"><span data-stu-id="652ca-224">Go to **Retail and Commerce \> Channels \> Stores \> All stores \> Statement/closing**, and for each store, set both the **Statement method** field and the **Closing method** field to **Shift**.</span></span>

<span data-ttu-id="652ca-225">Dette oppsettet bidrar til at Back Office-utdrag inneholder de samme transaksjonene som skift på salgsstedet, og at dataene blir summert etter dette skiftet.</span><span class="sxs-lookup"><span data-stu-id="652ca-225">This setup helps guarantee that back-office statements include the same transactions as shifts in the POS, and that the data is summarized by that shift.</span></span>

<span data-ttu-id="652ca-226">Hvis du vil ha mer informasjon om utdrag og avslutingsmetoder, kan du se [Butikkonfigurasjoner for detaljhandelsutdrag](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).</span><span class="sxs-lookup"><span data-stu-id="652ca-226">For more information about statement and closing methods, see [Store configurations for Retail statement](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).</span></span>