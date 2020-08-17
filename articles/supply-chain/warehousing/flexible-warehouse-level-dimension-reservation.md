---
title: Fleksibel retningslinje for dimensjonsreservasjon på lagernivå
description: Dette emnet beskriver retningslinjen for beholdningsreservasjon som lar virksomheter som selger partisporede produkter og kjører logistikken som WMS-aktiverte operasjoner, reservere spesifikke partier for kundesalgsordrer, selv om reservasjonshierarkiet som er assosiert med produktene, ikke tillater reservasjon av spesifikke partier.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 65304216b579b8def493d1e4218174cb9617013d
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652185"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="62ff9-103">Fleksibel retningslinje for dimensjonsreservasjon på lagernivå</span><span class="sxs-lookup"><span data-stu-id="62ff9-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62ff9-104">Når et hierarki for beholdningsreservasjon av "Parti under\[plassering\]"-typen er assosiert med produkter, kan bedrifter som selger partisporede produkter og kjører logistikken som operasjoner som er aktivert for Microsoft Dynamics 365 Warehouse Management System (WMS), ikke reservere spesifikke partier av disse produktene for kundesalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="62ff9-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="62ff9-105">På lignende måte kan ikke bestemte lisensplater reserveres for produkter i salgsordrer når disse produktene er knyttet til standard reservasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="62ff9-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="62ff9-106">Dette emnet beskriver retningslinjen for beholdningsreservasjon som lar disse virksomhetene reservere spesifikke partier eller lisensalter, selv når produktene er assosiert med et "Parti under\[plassering\]"-reservasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="62ff9-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="62ff9-107">Beholdningsreservasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="62ff9-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="62ff9-108">Dette avsnittet oppsummerer det eksisterende beholdningsreservasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="62ff9-109">Beholdningsreservasjonshierarkiet dikterer følgende: For lagringsdimensjoner angir etterspørselsordren de obligatoriske dimensjonene for sted, lager og beholdningsstatus, mens lagerlogikken har ansvar for å tilordne et sted til de forespurte kvantitetene og for å reservere stedet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="62ff9-110">Med andre ord gjelder følgende: I samhandlingene mellom etterspørselsordren og lagervirksomheten, forventes etterspørselsordren å indikere hvor ordren må sendes fra (det vil si hvilket sted og lager).</span><span class="sxs-lookup"><span data-stu-id="62ff9-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="62ff9-111">Lageret er deretter avhengig av logikken for å finne påkrevd kvantitet i lagerlokalene.</span><span class="sxs-lookup"><span data-stu-id="62ff9-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="62ff9-112">For å gjenspeile virksomhetens driftsmodell er sporingsdimensjoner (parti- og serienumre) imidlertid gjenstand for mer fleksibilitet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="62ff9-113">Et beholdningsreservasjonshierarki kan omfatte scenarioer der følgende betingelser gjelder:</span><span class="sxs-lookup"><span data-stu-id="62ff9-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="62ff9-114">Virksomheten avhenger av lagervirksomheten når det gjelder administrering av plukking av kvantiteter som har parti- eller serienumre, etter at kvantitetene er funnet i lagerlokalene.</span><span class="sxs-lookup"><span data-stu-id="62ff9-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="62ff9-115">Denne modellen henvises ofte til som *Parti under\[plassering\]*.</span><span class="sxs-lookup"><span data-stu-id="62ff9-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="62ff9-116">Den brukes vanligvis når et produkts parti- eller serienummeridentifikasjon ikke er viktig for kundene som legger inn etterspørselen hos det selgende selskapet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="62ff9-117">Hvis parti- eller serienumre er en del av en kundes ordrespesifikasjon, og de registreres i etterspørselsordren, blir lageroperasjonene som finner kvantitetene på lageret, begrenset av de spesifikke forespurte numrene og har ikke lov til å endre dem.</span><span class="sxs-lookup"><span data-stu-id="62ff9-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="62ff9-118">Denne modellen henvises til som *Parti over\[plassering\]*.</span><span class="sxs-lookup"><span data-stu-id="62ff9-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="62ff9-119">I disse scenarioene er utfordringen at bare ett beholdningsreservasjonshierarki kan tilordnes til hvert utgitte produkt.</span><span class="sxs-lookup"><span data-stu-id="62ff9-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="62ff9-120">For at WMS skal kunne håndtere sporede elementer gjelder derfor følgende: Etter at hierarkitildelingen bestemmer når parti- eller serienummeret skal reserveres (enten når etterspørselsordren tas imot eller under lagerplukkearbeidet), kan denne timingen ikke endres på et ad hoc-grunnlag.</span><span class="sxs-lookup"><span data-stu-id="62ff9-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="62ff9-121">Fleksibel reservasjon for partisporede varer</span><span class="sxs-lookup"><span data-stu-id="62ff9-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="62ff9-122">Forretningsscenario</span><span class="sxs-lookup"><span data-stu-id="62ff9-122">Business scenario</span></span>

<span data-ttu-id="62ff9-123">I dette scenarioet bruker et selskap en beholdningsstrategi der fullførte varer spores etter partinumre.</span><span class="sxs-lookup"><span data-stu-id="62ff9-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="62ff9-124">Dette selskapet bruker også WMS-arbeidsbelastning.</span><span class="sxs-lookup"><span data-stu-id="62ff9-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="62ff9-125">Fordi denne arbeidsbelastningen har velutstyrt logikk for planlegging og drift av lagerplukkings- og forsendelsesoperasjoner for partiaktiverte varer, er de fleste av de fullførte varene tilknyttet et "Parti under\[plassering\]"-beholdningsreservasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="62ff9-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="62ff9-126">Fordelen med denne typen driftsoppsett er at beslutninger (som faktisk er reservasjonsbeslutninger) om hvilke partier du skal plukkes, og hvor de skal settes på lageret, utsettes til lagerplukkingsoperasjonene starter.</span><span class="sxs-lookup"><span data-stu-id="62ff9-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="62ff9-127">De utføres ikke når kundens ordre legges inn.</span><span class="sxs-lookup"><span data-stu-id="62ff9-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="62ff9-128">Selv om "Parti under\[plassering\]"-reservasjonshierarkiet tjener selskapets forretningsmessige mål godt, krever mange av selskapets etablerte kunder det samme partiet som de kjøpte tidligere, når de bestiller produkter på nytt.</span><span class="sxs-lookup"><span data-stu-id="62ff9-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="62ff9-129">Derfor leter selskapet etter fleksibilitet i måten partireservasjonsreglene håndteres på, slik at det – avhengig av kundenes etterspørsel etter samme vare – oppstår følgende atferd:</span><span class="sxs-lookup"><span data-stu-id="62ff9-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="62ff9-130">Et partinummer kan registreres og reserveres når ordren tas imot av salgsprosessoren, og det kan ikke endres under lageroperasjoner og/eller tas imot av andre krav.</span><span class="sxs-lookup"><span data-stu-id="62ff9-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="62ff9-131">Denne atferden er med på å garantere at partinummeret som ble bestilt, sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="62ff9-132">Hvis partinummeret ikke er viktig for kunden, kan lageroperasjonen bestemme et partinummer under plukkearbeid, etter at salgsordreregistrering og reservasjon er utført.</span><span class="sxs-lookup"><span data-stu-id="62ff9-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="62ff9-133">Tillate reservering av et bestemt parti i salgsordren</span><span class="sxs-lookup"><span data-stu-id="62ff9-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="62ff9-134">For å imøtekomme ønsket fleksibilitet i partireservasjonsatferden for varer som er assosiert med et "Parti under\[plassering\]"-beholdningsreservasjonshierarki, må beholdningsledere merke av i **Tillat reservasjon på etterspørselsordre**-avmerkingsboksen for **Partinummer**-nivået på **Beholdningsreservasjonshierarkier**-siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Gjøre beholdningsreservasjonshierarkiet fleksibelt](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="62ff9-136">Når **Partinummer**-nivået i hierarkiet er valgt, vil alle dimensjoner over det nivået og opp gjennom **Plassering**-nivået valgt automatisk.</span><span class="sxs-lookup"><span data-stu-id="62ff9-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="62ff9-137">(Som standard er alle dimensjoner over **Plassering**-nivået forhåndsvalgt.) Denne atferden gjenspeiler logikken der alle dimensjoner i området mellom partinummeret og plasseringen også reserveres automatisk etter at du har reservert et spesifikt partinummer på ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="62ff9-138">**Tillat reservasjon på etterspørselsordre**-avmerkingsboksen gjelder bare for reservasjonshierarkinivåer som er under dimensjonen til lagerplasseringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="62ff9-139">**Partinummer** og **Nummerskilt** er de eneste nivåene i hierarkiet som er åpne for den fleksible reservasjonsretningslinjen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-139">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="62ff9-140">Med andre ord kan du ikke merke av for **Tillat reservasjon på etterspørselsordre** for nivået **Plassering** eller **Serienummer**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="62ff9-141">Hvis reservasjonshierarkiet inkluderer serienummerdimensjonen (som alltid må være under **Partinummer**-nivået), og hvis du har aktivert partispesifikk reservasjon for partinummeret, vil systemet fortsette å håndtere serienummerreservasjon og plukkeoperasjoner, basert på reglene som gjelder for "Serienr. under\[plassering\]"-reservasjonsretningslinjen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="62ff9-142">Du kan når som helst tillate partispesifikk reservasjon for et eksisterende "Parti under\[plassering\]"-reservasjonshierarki i distribusjonen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="62ff9-143">Denne endringen påvirker ikke reservasjoner og åpent lagerarbeid som ble opprettet før endringen fant sted.</span><span class="sxs-lookup"><span data-stu-id="62ff9-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="62ff9-144">**Tillat reservasjon på etterspørselsordre**-avmerkingsboksen kan imidlertid ikke tømmes hvis det finnes beholdningstransaksjoner med utstedelsestypen **Reservert bestilt**, **Reservert fysisk** eller **Bestilt** for én eller flere varer som er tilknyttet til dette reservasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="62ff9-145">Hvis eksisterende reservasjonshierarki for en vare ikke tillater partispesifikasjon på ordren, kan du tilordne den på nytt til et reservasjonshierarki som tillater partispesifikasjon, forutsatt at hierarkinivåstrukturen er lik i begge hierarkier.</span><span class="sxs-lookup"><span data-stu-id="62ff9-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="62ff9-146">Bruk **Endre reservasjonshierarki for varer**-funksjonen til å gjennomføre omtilordningen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="62ff9-147">Denne endringen kan være relevant når du vil forhindre fleksibel partireservering for et delsett av partisporede elementer, men tillate den for resten av produktporteføljen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="62ff9-148">Uavhengig av om du har merket av i **Tillat reservasjon på etterspørselsordre**-avmerkingsboksen, gjelder følgende: Hvis du ikke vil reservere et spesifikt partinummer for varen på en ordrelinje, vil standard lagerstyringslogikk som er gyldig for et "Parti under\[plassering\]"-reservasjonshierarki, fremdeles gjelde.</span><span class="sxs-lookup"><span data-stu-id="62ff9-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="62ff9-149">Reservere et bestemt partinummer for en kundeordre</span><span class="sxs-lookup"><span data-stu-id="62ff9-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="62ff9-150">Etter at "Parti under\[plassering\]"-beholdningsreservasjonshierarki for en partisporet vare er satt opp for å tillate reservasjon av spesifikke partinumre på salgsordrer, kan salgsordreprosessorer ta imot kundeordrer for samme vare på en av følgende måter, avhengig av kundens forespørsel:</span><span class="sxs-lookup"><span data-stu-id="62ff9-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="62ff9-151">**Angi ordredetaljer uten å angi et partinummer** – Denne fremgangsmåten skal brukes når produktets partispesifikasjon ikke er viktig for kunden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="62ff9-152">Alle eksisterende prosesser som er knyttet til håndtering av en ordre av denne typen i systemet, forblir uendret.</span><span class="sxs-lookup"><span data-stu-id="62ff9-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="62ff9-153">Ingen ekstra hensyn kreves fra brukerne.</span><span class="sxs-lookup"><span data-stu-id="62ff9-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="62ff9-154">**Angi ordredetaljer og reserver et bestemt partinummer** – Denne fremgangsmåten skal brukes når kunden ber om et bestemt parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="62ff9-155">Vanligvis vil kunder be om et bestemt parti når de ombestiller et produkt som de har kjøpt tidligere.</span><span class="sxs-lookup"><span data-stu-id="62ff9-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="62ff9-156">Denne typen partispesifikk reservasjon omtales som *Ordreigangsatt reservasjon*.</span><span class="sxs-lookup"><span data-stu-id="62ff9-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="62ff9-157">Følgende sett med regler er gyldig når kvantiteter behandles, og et partinummer er bundet til en bestemt ordre:</span><span class="sxs-lookup"><span data-stu-id="62ff9-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="62ff9-158">For å tillate reservasjon av et spesifikt partinummer for en vare under "Parti under\[plassering\]"-reservasjonsretningslinjen må systemet reservere alle dimensjoner opp gjennom plasseringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="62ff9-159">Dette området inkluderer vanligvis nummerskiltdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="62ff9-160">Plasseringsdirektiver brukes ikke når det opprettes plukkarbeid for en salgslinje som bruker ordrebundet partireservering.</span><span class="sxs-lookup"><span data-stu-id="62ff9-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="62ff9-161">Under lagerbehandling av arbeid for ordrebundne partier har verken brukeren eller systemet lov til å endre partinummeret.</span><span class="sxs-lookup"><span data-stu-id="62ff9-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="62ff9-162">(Denne behandlingen omfatter unntakshåndtering.)</span><span class="sxs-lookup"><span data-stu-id="62ff9-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="62ff9-163">Det følgende eksempelet viser ende-til-ende-flyten.</span><span class="sxs-lookup"><span data-stu-id="62ff9-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="62ff9-164">Eksempelscenario: Tildeling av partinummer</span><span class="sxs-lookup"><span data-stu-id="62ff9-164">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="62ff9-165">For dette eksempelet må demonstrasjonsdata være installert, og du må bruke **USMF**-demonstrasjonsdataselskapet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="62ff9-166">Sette opp et beholdningsreservasjonshierarki for å tillate partispesifikk reservasjon</span><span class="sxs-lookup"><span data-stu-id="62ff9-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="62ff9-167">Gå til **Lagerstyring** \> **Oppsett** \> **Beholdning \> Reservasjonshierarki**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="62ff9-168">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-168">Select **New**.</span></span>
3. <span data-ttu-id="62ff9-169">I **Navn**-feltet skriver du inn et navn (for eksempel **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="62ff9-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="62ff9-170">I **Beskrivelse**-feltet skriver du inn en beskrivelse (for eksempel **Parti under fleksibelt**).</span><span class="sxs-lookup"><span data-stu-id="62ff9-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="62ff9-171">I **Valgt**-feltet velger du **Serienummer** og **Eier**, og velg deretter venstre pilknapp for å flytte dem til **Tilgjengelig**-feltet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="62ff9-172">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-172">Select **OK**.</span></span>
7. <span data-ttu-id="62ff9-173">I raden for **Partinummer**-dimensjonsnivået merker du av i **Tillat reservasjon på etterspørselsordre**-avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="62ff9-174">**Nummerskilt**- og **Plassering**-nivåene velges automatisk, og du kan ikke fjerne avmerkingen i avmerkingsboksene for dem.</span><span class="sxs-lookup"><span data-stu-id="62ff9-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="62ff9-175">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="62ff9-176">Opprette et nytt frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="62ff9-176">Create a new released product</span></span>

1. <span data-ttu-id="62ff9-177">Angi de tre hoveddataparameterne for produktet ved å bruke disse verdiene:</span><span class="sxs-lookup"><span data-stu-id="62ff9-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="62ff9-178">I **Lagringsdimensjonsgruppe**-feltet velger du **Lager**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="62ff9-179">I **Sporingsdimensjonsgruppe**-feltet velger du **Parti-fys**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="62ff9-180">I **Reservasjonshierarki**-feltet velger du **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="62ff9-181">Opprett to partinumre, for eksempel **B11** og **B22**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="62ff9-182">Legg til varekvantiteter i beholdningen på lager ved hjelp av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="62ff9-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="62ff9-183">Lager</span><span class="sxs-lookup"><span data-stu-id="62ff9-183">Warehouse</span></span> | <span data-ttu-id="62ff9-184">Partinummer</span><span class="sxs-lookup"><span data-stu-id="62ff9-184">Batch number</span></span> | <span data-ttu-id="62ff9-185">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="62ff9-185">Location</span></span> | <span data-ttu-id="62ff9-186">Nummerskilt</span><span class="sxs-lookup"><span data-stu-id="62ff9-186">License plate</span></span> | <span data-ttu-id="62ff9-187">Antall</span><span class="sxs-lookup"><span data-stu-id="62ff9-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="62ff9-188">24</span><span class="sxs-lookup"><span data-stu-id="62ff9-188">24</span></span>        | <span data-ttu-id="62ff9-189">B11</span><span class="sxs-lookup"><span data-stu-id="62ff9-189">B11</span></span>          | <span data-ttu-id="62ff9-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="62ff9-190">BULK-001</span></span> | <span data-ttu-id="62ff9-191">Ingen</span><span class="sxs-lookup"><span data-stu-id="62ff9-191">None</span></span>          | <span data-ttu-id="62ff9-192">10</span><span class="sxs-lookup"><span data-stu-id="62ff9-192">10</span></span>       |
    | <span data-ttu-id="62ff9-193">24</span><span class="sxs-lookup"><span data-stu-id="62ff9-193">24</span></span>        | <span data-ttu-id="62ff9-194">B11</span><span class="sxs-lookup"><span data-stu-id="62ff9-194">B11</span></span>          | <span data-ttu-id="62ff9-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="62ff9-195">FL-001</span></span>   | <span data-ttu-id="62ff9-196">LP11</span><span class="sxs-lookup"><span data-stu-id="62ff9-196">LP11</span></span>          | <span data-ttu-id="62ff9-197">10</span><span class="sxs-lookup"><span data-stu-id="62ff9-197">10</span></span>       |
    | <span data-ttu-id="62ff9-198">24</span><span class="sxs-lookup"><span data-stu-id="62ff9-198">24</span></span>        | <span data-ttu-id="62ff9-199">B22</span><span class="sxs-lookup"><span data-stu-id="62ff9-199">B22</span></span>          | <span data-ttu-id="62ff9-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="62ff9-200">FL-002</span></span>   | <span data-ttu-id="62ff9-201">LP22</span><span class="sxs-lookup"><span data-stu-id="62ff9-201">LP22</span></span>          | <span data-ttu-id="62ff9-202">10</span><span class="sxs-lookup"><span data-stu-id="62ff9-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="62ff9-203">Angi salgsordredetaljer</span><span class="sxs-lookup"><span data-stu-id="62ff9-203">Enter sales order details</span></span>

1. <span data-ttu-id="62ff9-204">Gå til **Salg og markedsføring** \> **Salgsordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="62ff9-205">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-205">Select **New**.</span></span>
3. <span data-ttu-id="62ff9-206">På salgsordretoppteksten, i **Kundekonto**-feltet angir du **US-003**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="62ff9-207">Legg til en linje for den nye varen, og angi **10** som kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="62ff9-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="62ff9-208">Sørg for at **Lager**-feltet er satt til **24**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="62ff9-209">På **Salgsordrelinjer**-hurtigfanen velger du **Beholdning**, og går deretter til **Vedlikehold**-gruppen og velger **Partireservasjon**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="62ff9-210">**Partireservasjon**-siden viser en liste over partier som er tilgjengelige for reservasjon for ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="62ff9-211">For dette eksempelet viser den en kvantitet på **20** for partinummer **B11** og en kvantitet på **10** for partinummer **B22**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="62ff9-212">Vær oppmerksom på at **Partireservasjon**-siden ikke kan åpnes fra en linje hvis varen på denne linjen er assosiert med "Parti under\[plassering\]"-reservasjonshierarki med mindre den er satt opp for å tillate partispesifikk reservasjon.</span><span class="sxs-lookup"><span data-stu-id="62ff9-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62ff9-213">Hvis du vil reservere et bestemt parti for en salgsordre, må du bruke **Partireservasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="62ff9-214">Hvis du oppgir partinummeret direkte på salgsordrelinjen, vil systemet fungere som om du skrev inn en spesifikk partiverdi for en vare som er underlagt "Parti under\[plassering\]"-reservasjonsretningslinjen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="62ff9-215">Når du lagrer linjen, får du en advarselmelding.</span><span class="sxs-lookup"><span data-stu-id="62ff9-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="62ff9-216">Hvis du bekrefter at partinummeret skal angis direkte på ordrelinjen, vil ikke linjen bli håndtert av den vanlige lagerbehandlingslogikken.</span><span class="sxs-lookup"><span data-stu-id="62ff9-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="62ff9-217">Hvis du reserverer kvantiteten fra **Reservasjon**-siden, vil ikke noe spesifikt parti bli reservert, og kjøringen av lageroperasjoner for linjen vil følge reglene som gjelder under "Parti under\[plassering\]"-reservasjonsretningslinjen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="62ff9-218">Generelt fungerer og samhandles denne siden med på samme måte som den fungerer og samhandles med for varer som har et tilknyttet reservasjonshierarki i "Parti over\[plassering\]"-typen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="62ff9-219">Følgende unntak gjelder imidlertid:</span><span class="sxs-lookup"><span data-stu-id="62ff9-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="62ff9-220">**Partinumre bundet til kildelinjen**-hurtigfanen viser partinumrene som er reservert for ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="62ff9-221">Partiverdiene i rutenettet vises gjennom oppfyllingssyklusen til ordrelinjen, inkludert lagerbehandlingsstadiene.</span><span class="sxs-lookup"><span data-stu-id="62ff9-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="62ff9-222">På **Oversikt**-hurtigfanen vises vanlig bestillingslinjereservasjon (det vil si reservasjon som utføres for dimensjonene over **Plassering**-nivået) derimot i rutenettet opp til tidspunktet lagerarbeidet opprettes på.</span><span class="sxs-lookup"><span data-stu-id="62ff9-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="62ff9-223">Deretter overtar arbeidsenheten linjereservasjonen, og linjereservasjonen vises ikke lenger på siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="62ff9-224">**Partinumre bundet til kildelinjen**-hurtigfanen bidrar til å garantere at salgsordreprosessoren kan vise partinumrene som ble bundet til kundens ordre, når som helst i løpet av livssyklusen, opp gjennom faktureringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="62ff9-225">I tillegg til å reservere et bestemt parti kan en bruker manuelt velge den partispesifikke plasseringen og nummerskiltet i stedet for å la systemet velge dem automatisk.</span><span class="sxs-lookup"><span data-stu-id="62ff9-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="62ff9-226">Denne funksjonen er knyttet til utformingen av den ordreigangsatte partireservasjonsmekanismen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="62ff9-227">Som nevnt tidligere, gjelder følgende: Når et partinummer er reservert for en vare under "Parti under\[plassering\]"-reservasjonsretningslinjen må systemet reservere alle dimensjoner opp gjennom plasseringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="62ff9-228">Derfor vil lagerarbeid ha de samme lagringsdimensjonene som ble reservert av brukerne som jobbet med ordrene, og det kan hende at det ikke alltid representerer varelagerplasseringen som er praktisk, eller til og med mulig, for plukkeoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="62ff9-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="62ff9-229">Hvis ordreprosessorer er klare over lagerbegrensningene, kan det være lurt manuelt å velge de spesifikke plasseringene og nummerskiltene når de reserverer et parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="62ff9-230">I slike tilfeller må brukeren bruke **Visningsdimensjoner**-funksjonaliteten på sidetoppteksten og legge til plasseringen og nummerskiltet i rutenettet på **Oversikt**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="62ff9-231">På **Partireservasjon**-siden velger du linjen for parti **B11**, og velger deretter **Reserver linje**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="62ff9-232">Det er ikke angitt noen logikk for tilordning av plasseringen og nummerskilt under automatisk reservasjon.</span><span class="sxs-lookup"><span data-stu-id="62ff9-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="62ff9-233">Du kan angi kvantiteten manuelt i **Reservasjon**-feltet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="62ff9-234">Vær oppmerksom på at **Partinumre bundet til kildelinjen**-hurtigfanen, parti **B11** vises som **Bind**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Binde et spesifikt partinummer til en salgsordrelinje på Partireservasjon-siden](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="62ff9-236">Reservasjon av kvantiteten på en salgsordrelinje kan utføres på tvers av flere partier.</span><span class="sxs-lookup"><span data-stu-id="62ff9-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="62ff9-237">På samme måte kan reservasjon av samme parti utføres mot flere plasseringer og nummerskilt (hvis nummerskilt er aktivert for plasseringene).</span><span class="sxs-lookup"><span data-stu-id="62ff9-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="62ff9-238">Reservasjon av et bestemt parti for kvantiteten på en salgsordrelinje kan også være delvis.</span><span class="sxs-lookup"><span data-stu-id="62ff9-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="62ff9-239">Den totale kvantiteten på 100 enheter kan for eksempel reserveres slik at et spesifikt parti bindes til 20 enheter, mens 80 enheter reserveres på stedet og lagernivåer for ethvert tilgjengelig parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="62ff9-240">I dette tilfellet vil WMS håndtere plukkoperasjoner ved hjelp av to separate arbeidslinjer.</span><span class="sxs-lookup"><span data-stu-id="62ff9-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="62ff9-241">Gå til **Administrering av produktinformasjon** \> **Produkter** \> **Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="62ff9-242">Velg varen, og velg deretter **Administrer beholdning** \> **Vis** \> **Transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Ordreigangsatt reservasjon som lagertransaksjonstype](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="62ff9-244">Gjennomgå varens lagertransaksjoner som er knyttet til salgsordrelinjereservasjonen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="62ff9-245">En transaksjon der **Referanse**-feltet er satt til **Salgsordre** og **Utsted**-feltet er satt til **Reservert fysisk**, representerer ordrelinjereservasjonen for beholdningsdimensjonene over **Plassering**-nivået.</span><span class="sxs-lookup"><span data-stu-id="62ff9-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="62ff9-246">I henhold til varens beholdningsreservasjonshierarki er disse dimensjonene sted, lager og beholdningsstatus.</span><span class="sxs-lookup"><span data-stu-id="62ff9-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="62ff9-247">En transaksjon der **Referanse**-feltet er satt til **Ordreigangsatt reservasjon** og **Utsted**-feltet er satt til **Reservert fysisk**, representerer ordrelinjereservasjonen for det spesifikke partiet og alle beholdningsdimensjonene over det.</span><span class="sxs-lookup"><span data-stu-id="62ff9-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="62ff9-248">I henhold til varens beholdningsreservasjonshierarki er disse dimensjonene partinummer og plassering.</span><span class="sxs-lookup"><span data-stu-id="62ff9-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="62ff9-249">I dette eksempelet er plasseringen **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="62ff9-250">I salgsordretoppteksten velger du **Lager** \> **Handlinger** \> **Frigi til lager**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="62ff9-251">Ordrelinjen er nå bølgete, og det opprettes en belastning og et arbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="62ff9-252">Gjennomgå og behandle lagerarbeid som har ordreigangsatte partinumre</span><span class="sxs-lookup"><span data-stu-id="62ff9-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="62ff9-253">I **Salgsordrer**-hurtigfanen velger du **Lager** \> **Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="62ff9-254">Arbeidet som håndterer plukkoperasjonen for partikvantiteter som er bundet til salgsordrelinjen, har følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="62ff9-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="62ff9-255">For opprettelse av arbeid bruker systemet arbeidsmaler, men ikke plasseringsdirektiver.</span><span class="sxs-lookup"><span data-stu-id="62ff9-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="62ff9-256">Alle standardinnstillingene som er definert for arbeidsmaler, for eksempel et maksimalt antall plukklinjer eller en bestemt måleenhet, brukes for å bestemme når nytt arbeid skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="62ff9-257">Reglene som er assosiert med plasseringsdirektiver for identifisering av plukkplasseringer blir ikke vurdert, fordi den ordreigangsatte reservasjonen allerede angir alle beholdningsdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="62ff9-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="62ff9-258">Disse beholdningsdimensjonene inkluderer dimensjonene på lageroppbevaringsnivået.</span><span class="sxs-lookup"><span data-stu-id="62ff9-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="62ff9-259">Derfor arver arbeidet disse dimensjonene uten å måtte sjekke plasseringsdirektiver.</span><span class="sxs-lookup"><span data-stu-id="62ff9-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="62ff9-260">Partinummeret vises ikke på plukklinjen (noe som også er tilfelle for arbeidslinjen som opprettes for en vare som har et tilknyttet "Parti over\[plassering\]"-reservasjonshierarki). I stedet vises "fra"-partinummeret og alle andre lagringsdimensjoner på arbeidslinjens arbeidsbeholdningstransaksjon som det henvises til fra de tilhørende beholdningstransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="62ff9-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Lagerbeholdningstransaksjon for arbeid som stammer fra ordreigangsatt reservasjon](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="62ff9-262">Etter at arbeidet er opprettet, blir varens beholdningstransaksjon der **Referanse**-feltet er satt til **Ordreigangsatt reservasjon**, fjernet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="62ff9-263">Beholdningstransaksjonen der **Referanse**-feltet er satt til **Arbeid**, inneholder nå den fysiske reservasjonen for alle beholdningsdimensjoner for kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="62ff9-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="62ff9-264">Lageroperasjoner kan fortsette å håndtere utførelsen av arbeidet på vanlig måte.</span><span class="sxs-lookup"><span data-stu-id="62ff9-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="62ff9-265">Instruksjonene på mobilenheten vil imidlertid instruere arbeideren om å velge et bestemt partinummer.</span><span class="sxs-lookup"><span data-stu-id="62ff9-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="62ff9-266">I lagermiljøer der plasseringene er nummerskiltkontrollert, gjelder følgende: Etter at en arbeider har nådd en plassering som lagrer det samme partiet på flere nummerskilt, kan han eller hun velge fra et hvilket som helst nummerskilt som ikke allerede er reservert (for eksempel av en annen ordreigangsatt reservasjon eller arbeid som stammer fra en reservasjon av denne typen.)</span><span class="sxs-lookup"><span data-stu-id="62ff9-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="62ff9-267">Hvis det viser seg at det blir upraktisk å velge fra plasseringen som er spesifisert på arbeidslinjen, kan lageroperatørene bruke en av følgende handlinger for å omdirigere plukking av det spesifikke partiet fra en mer praktisk plassering:</span><span class="sxs-lookup"><span data-stu-id="62ff9-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="62ff9-268">Standardhandlingen **Overstyr plassering** på en mobilenhet (forutsatt at lagerarbeiderens **Tillat overstyring av plukkplassering**-innstilling er aktivert)</span><span class="sxs-lookup"><span data-stu-id="62ff9-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="62ff9-269">**Endre plassering**-handlingen på**Arbeidslistedetaljer**-siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="62ff9-270">Fullfør plukking og plassering av arbeidet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="62ff9-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="62ff9-271">Antallet **10** for partinummer **B11** er nå valgt for salgsordrelinjen og plassert i **Båsdør**-plasseringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="62ff9-272">På dette tidspunktet er det klart til å lastes på lastebilen og sendes til kundens adresse.</span><span class="sxs-lookup"><span data-stu-id="62ff9-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="62ff9-273">Fleksibel nummerskiltreservering</span><span class="sxs-lookup"><span data-stu-id="62ff9-273">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="62ff9-274">Forretningsscenario</span><span class="sxs-lookup"><span data-stu-id="62ff9-274">Business scenario</span></span>

<span data-ttu-id="62ff9-275">I dette scenariet bruker et firma lagerstyring og arbeidsbehandling, og håndterer belastningsplanlegging på nivået for individuelle paller/beholdere utenfor Supply Chain Management før arbeidet opprettes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-275">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="62ff9-276">Disse beholderne representeres av nummerskilt i lager dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="62ff9-276">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="62ff9-277">Derfor må spesifikke nummerskilt være forhåndstilordnet til salgsordrelinjer før plukkearbeidet utføres, for denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="62ff9-277">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="62ff9-278">Firmaet ser etter fleksibilitet i måten regler for nummerskiltreservasjon behandles på, slik at følgende virkemåter skjer:</span><span class="sxs-lookup"><span data-stu-id="62ff9-278">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="62ff9-279">Et nummerskilt kan registreres og reserveres når ordren tas imot av salgsprosessoren, og det kan ikke tas imot av andre krav.</span><span class="sxs-lookup"><span data-stu-id="62ff9-279">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="62ff9-280">Denne atferden er med på å garantere at numerskiltet som var planlagt, sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-280">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="62ff9-281">Hvis nummerskiltet ikke allerede er tilordnet til en salgsordrelinje, kan lagerpersonell velge et nummerskilt under plukkingen, etter at salgsordreregistreringen og reservering er fullført.</span><span class="sxs-lookup"><span data-stu-id="62ff9-281">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="62ff9-282">Aktivere fleksibel nummerskiltreservering</span><span class="sxs-lookup"><span data-stu-id="62ff9-282">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="62ff9-283">Før du kan bruke fleksibel nummerskiltreservering, må to funksjoner aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-283">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="62ff9-284">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for funksjonene og aktivere dem hvis nødvendig.</span><span class="sxs-lookup"><span data-stu-id="62ff9-284">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="62ff9-285">Du må aktivere funksjonene i følgende rekkefølge:</span><span class="sxs-lookup"><span data-stu-id="62ff9-285">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="62ff9-286">**Funksjonsnavn:** *Fleksibel dimensjonsreservasjonspolicy for lagernivå*</span><span class="sxs-lookup"><span data-stu-id="62ff9-286">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="62ff9-287">**Funksjonsnavn:** *Fleksibel ordreigangsatt nummerskiltreservering*</span><span class="sxs-lookup"><span data-stu-id="62ff9-287">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="62ff9-288">Reservere et bestemt nummerskilt på salgsordren</span><span class="sxs-lookup"><span data-stu-id="62ff9-288">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="62ff9-289">Hvis du vil aktivere nummerskiltreservering for en ordre, må du merke av for **Tillat reservasjon på etterspørselsordre** for **Nummerskilt**-nivået på siden **Beholdningsreservasjonshierarkier** for hierarkiet som er knyttet til den aktuelle varen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-289">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Siden Beholdningsreservasjonshierarkier for et fleksibelt hierarki for nummerskiltreservasjon](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="62ff9-291">Du kan aktivere reservasjon av nummerskilt for ordren på et hvilket som helst sted i distribusjonen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-291">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="62ff9-292">Denne endringen påvirker ikke reservasjoner eller åpent lagerarbeid som ble opprettet før endringen fant sted.</span><span class="sxs-lookup"><span data-stu-id="62ff9-292">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="62ff9-293">Du kan imidlertid ikke fjerne merket for **Tillat reservasjon på etterspørselsordre** hvis det finnes åpne utgående beholdningstransaksjoner med utstedelsesstatusen *På bestilling*, *Reservert bestilt* eller *Reservert fysisk* for én eller flere varer som er tilknyttet til dette reservasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-293">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="62ff9-294">Selv om det er merket av for **Tillat reservasjon på etterspørselsordre** for **Nummerskilt**-nivået, er det fremdeles mulig *ikke* å reservere et bestemt nummerskilt i ordren.</span><span class="sxs-lookup"><span data-stu-id="62ff9-294">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="62ff9-295">I dette tilfellet gjelder standard lageroperasjonslogikk som er gyldig for reservasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-295">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="62ff9-296">Hvis du vil reservere et bestemt nummerskilt, må du bruke en prosess av typen [åpen dataprotokoll (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md). I appen kan du foreta denne reservasjonen direkte fra en salgsordre ved å bruke alternativet **Ordreigangsatte reservasjoner per nummerskilt** for kommandoen **Åpne i Excel**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-296">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="62ff9-297">I enhetsdataene som åpnes i Excel-tillegget, må du angi følgende data for reservasjon, og deretter velge **Publiser** for å sende dataene tilbake til Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="62ff9-297">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="62ff9-298">Referanse (bare *Salgsordre*-verdien støttes.)</span><span class="sxs-lookup"><span data-stu-id="62ff9-298">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="62ff9-299">Ordrenummer (verdien kan avledes fra partiet).</span><span class="sxs-lookup"><span data-stu-id="62ff9-299">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="62ff9-300">Parti-ID</span><span class="sxs-lookup"><span data-stu-id="62ff9-300">Lot ID</span></span>
- <span data-ttu-id="62ff9-301">Nummerskilt</span><span class="sxs-lookup"><span data-stu-id="62ff9-301">License plate</span></span>
- <span data-ttu-id="62ff9-302">Antall</span><span class="sxs-lookup"><span data-stu-id="62ff9-302">Quantity</span></span>

<span data-ttu-id="62ff9-303">Hvis du må reservere et bestemt nummerskilt for en partisporet vare, bruker du **Partireservasjon**-siden som beskrevet i dele [Angi salgsordredetaljer](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="62ff9-303">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="62ff9-304">Når salgsordrelinjen som bruker en tildelt nummerskiltreservasjon, behandles av lageroperasjoner, brukes ikke lokasjonsdirektiver.</span><span class="sxs-lookup"><span data-stu-id="62ff9-304">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="62ff9-305">Hvis en lagerarbeidsvare består av linjer som er lik en fullstendig pall og har antall igangsatt av nummerskilt, kan du optimalisere plukkeprosessen ved å bruke menyelementet for en mobilenhet der alternativet **Behandle etter nummerskilt** er satt til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="62ff9-305">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="62ff9-306">En lagerarbeider kan deretter skanne et nummerskilt for å fullføre en plukking i stedet for å måtte skanne varene fra arbeidet én etter én.</span><span class="sxs-lookup"><span data-stu-id="62ff9-306">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Menyelementet for mobilenhet der alternativet Behandle etter nummerskilt er satt til Ja](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="62ff9-308">Fordi funksjonen **Behandle etter nummerskilt** ikke støtter arbeid som dekker flere paller, er det bedre å ha et separat arbeidselement for forskjellige nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="62ff9-308">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="62ff9-309">Hvis du vil bruke denne fremgangsmåten, legger du til eltet **ID for ordreigangsatt nummerskilt** som et arbeidshodeskift på **Arbeidsmal**-siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-309">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="62ff9-310">Eksempelscenario: Definere og behandle en ordreigangsatt nummerskiltreservering</span><span class="sxs-lookup"><span data-stu-id="62ff9-310">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="62ff9-311">Dette scenarioet viser hvordan du definerer og behandler en ordreigangsatt nummerskiltreservering.</span><span class="sxs-lookup"><span data-stu-id="62ff9-311">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="62ff9-312">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="62ff9-312">Make demo data available</span></span>

<span data-ttu-id="62ff9-313">Dette scenarioet refererer til verdier og poster som er inkludert i standard demodata som leveres for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="62ff9-313">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="62ff9-314">Hvis du vil arbeide deg gjennom dette scenariet ved å bruke verdiene som presenteres her, må du arbeide i et miljø der standard demodata er installert.</span><span class="sxs-lookup"><span data-stu-id="62ff9-314">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="62ff9-315">Du må også angi den juridiske enheten til **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="62ff9-315">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="62ff9-316">Opprette et lagerreservasjonshierarki som tillater nummerskiltreservering</span><span class="sxs-lookup"><span data-stu-id="62ff9-316">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="62ff9-317">Gå til **Lagerstyring \> Oppsett \> Beholdning \> Reservasjonshierarki**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-317">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="62ff9-318">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-318">Select **New**.</span></span>
1. <span data-ttu-id="62ff9-319">I **Navn**-feltet angir du en verdi (for eksempel *FlexibleLP*).</span><span class="sxs-lookup"><span data-stu-id="62ff9-319">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="62ff9-320">I **Beskrivelse**-feltet angir du en verdi (for eksempel *Fleksibel nummerskiltreservasjon*).</span><span class="sxs-lookup"><span data-stu-id="62ff9-320">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="62ff9-321">I **Valgt**-listen velger du **Partinummer**, **Serienummer** og **Eier**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-321">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="62ff9-322">Velg **Fjern**-knappen ![bakoverpil](media/backward-button.png) for å flytte de valgte oppføringene til listen **Tilgjengelig**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-322">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="62ff9-323">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-323">Select **OK**.</span></span>
1. <span data-ttu-id="62ff9-324">I raden for **Nummerskilt**-dimensjonsnivået merker du av i **Tillat reservasjon på etterspørselsordre**-avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-324">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="62ff9-325">**Plassering**-nivået velges automatisk, og du kan ikke fjerne avmerkingen i avmerkingsboksen for det.</span><span class="sxs-lookup"><span data-stu-id="62ff9-325">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="62ff9-326">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-326">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="62ff9-327">Opprette to frigitte produkter</span><span class="sxs-lookup"><span data-stu-id="62ff9-327">Create two released products</span></span>

1. <span data-ttu-id="62ff9-328">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-328">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="62ff9-329">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="62ff9-329">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="62ff9-330">Angi følgende verdier i dialogboksen **Nytt frigitt produkt**:</span><span class="sxs-lookup"><span data-stu-id="62ff9-330">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="62ff9-331">**Produktnummer:** *Vare 1*</span><span class="sxs-lookup"><span data-stu-id="62ff9-331">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="62ff9-332">**Varenummer:** *Vare 1*</span><span class="sxs-lookup"><span data-stu-id="62ff9-332">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="62ff9-333">**Varemodellgruppe:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="62ff9-333">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="62ff9-334">**Varegruppe:** *Lyd*</span><span class="sxs-lookup"><span data-stu-id="62ff9-334">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="62ff9-335">**Lagringsdimensjonsgruppe:** *Bølge*</span><span class="sxs-lookup"><span data-stu-id="62ff9-335">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="62ff9-336">**Sporingsdimensjonsgruppe:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="62ff9-336">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="62ff9-337">**Reservasjonshierarki:** *Fleksibelt nummerskilt*</span><span class="sxs-lookup"><span data-stu-id="62ff9-337">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="62ff9-338">Velg **OK** for å opprette produktet og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-338">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="62ff9-339">Det nye produktet åpnes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-339">The new product is opened.</span></span> <span data-ttu-id="62ff9-340">På **Lager**-hurtigfanen angir du *ea* i **Sekvensgruppe-ID for enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-340">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="62ff9-341">Gjenta de forrige trinnene for å opprette et nytt produkt som har de samme innstillingene, men sett feltene **Produktnumer** og **Varenummer** til *Vare 2*.</span><span class="sxs-lookup"><span data-stu-id="62ff9-341">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="62ff9-342">I handlingsruten i kategorien **Administrer lager** i gruppen **Visning** velger du **Lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-342">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="62ff9-343">Velg deretter **Antallsjustering**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-343">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="62ff9-344">Juster lagerbeholdningen for de nye varene slik det er angitt i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="62ff9-344">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="62ff9-345">Artikkel</span><span class="sxs-lookup"><span data-stu-id="62ff9-345">Item</span></span>  | <span data-ttu-id="62ff9-346">Lager</span><span class="sxs-lookup"><span data-stu-id="62ff9-346">Warehouse</span></span> | <span data-ttu-id="62ff9-347">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="62ff9-347">Location</span></span> | <span data-ttu-id="62ff9-348">Nummerskilt</span><span class="sxs-lookup"><span data-stu-id="62ff9-348">License plate</span></span> | <span data-ttu-id="62ff9-349">Antall</span><span class="sxs-lookup"><span data-stu-id="62ff9-349">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="62ff9-350">Vare 1</span><span class="sxs-lookup"><span data-stu-id="62ff9-350">Item1</span></span> | <span data-ttu-id="62ff9-351">24</span><span class="sxs-lookup"><span data-stu-id="62ff9-351">24</span></span>        | <span data-ttu-id="62ff9-352">FL-010</span><span class="sxs-lookup"><span data-stu-id="62ff9-352">FL-010</span></span>   | <span data-ttu-id="62ff9-353">LP01</span><span class="sxs-lookup"><span data-stu-id="62ff9-353">LP01</span></span>          | <span data-ttu-id="62ff9-354">10</span><span class="sxs-lookup"><span data-stu-id="62ff9-354">10</span></span>       |
    | <span data-ttu-id="62ff9-355">Vare 1</span><span class="sxs-lookup"><span data-stu-id="62ff9-355">Item1</span></span> | <span data-ttu-id="62ff9-356">24</span><span class="sxs-lookup"><span data-stu-id="62ff9-356">24</span></span>        | <span data-ttu-id="62ff9-357">FL-011</span><span class="sxs-lookup"><span data-stu-id="62ff9-357">FL-011</span></span>   | <span data-ttu-id="62ff9-358">LP02</span><span class="sxs-lookup"><span data-stu-id="62ff9-358">LP02</span></span>          | <span data-ttu-id="62ff9-359">10</span><span class="sxs-lookup"><span data-stu-id="62ff9-359">10</span></span>       |
    | <span data-ttu-id="62ff9-360">Vare 2</span><span class="sxs-lookup"><span data-stu-id="62ff9-360">Item2</span></span> | <span data-ttu-id="62ff9-361">24</span><span class="sxs-lookup"><span data-stu-id="62ff9-361">24</span></span>        | <span data-ttu-id="62ff9-362">FL-010</span><span class="sxs-lookup"><span data-stu-id="62ff9-362">FL-010</span></span>   | <span data-ttu-id="62ff9-363">LP01</span><span class="sxs-lookup"><span data-stu-id="62ff9-363">LP01</span></span>          | <span data-ttu-id="62ff9-364">5</span><span class="sxs-lookup"><span data-stu-id="62ff9-364">5</span></span>        |
    | <span data-ttu-id="62ff9-365">Vare 2</span><span class="sxs-lookup"><span data-stu-id="62ff9-365">Item2</span></span> | <span data-ttu-id="62ff9-366">24</span><span class="sxs-lookup"><span data-stu-id="62ff9-366">24</span></span>        | <span data-ttu-id="62ff9-367">FL-011</span><span class="sxs-lookup"><span data-stu-id="62ff9-367">FL-011</span></span>   | <span data-ttu-id="62ff9-368">LP02</span><span class="sxs-lookup"><span data-stu-id="62ff9-368">LP02</span></span>          | <span data-ttu-id="62ff9-369">5</span><span class="sxs-lookup"><span data-stu-id="62ff9-369">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="62ff9-370">Du må opprette de to nummerskiltene og bruke lokasjoner som tillater blandede varer, for eksempel *FL-010* og *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="62ff9-370">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="62ff9-371">Opprette en salgsordre og reservere et bestemt nummerskilt</span><span class="sxs-lookup"><span data-stu-id="62ff9-371">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="62ff9-372">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-372">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="62ff9-373">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-373">Select **New**.</span></span>
1. <span data-ttu-id="62ff9-374">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="62ff9-374">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="62ff9-375">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="62ff9-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="62ff9-376">**Lager:** *24*</span><span class="sxs-lookup"><span data-stu-id="62ff9-376">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="62ff9-377">Velg **OK** for lukke dialogboksen **Opprett salgsordre** og åpne den nye salgsorden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-377">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="62ff9-378">På hurtigfanen **Salgsordrelinjer** legger du til en linje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="62ff9-378">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="62ff9-379">**Varenummer:** *Vare 1*</span><span class="sxs-lookup"><span data-stu-id="62ff9-379">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="62ff9-380">**Antall:** *10*</span><span class="sxs-lookup"><span data-stu-id="62ff9-380">**Quantity:** *10*</span></span>

1. <span data-ttu-id="62ff9-381">Legg til en ny salgsordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="62ff9-381">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="62ff9-382">**Varenummer:** *Vare 2*</span><span class="sxs-lookup"><span data-stu-id="62ff9-382">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="62ff9-383">**Antall:** *5*</span><span class="sxs-lookup"><span data-stu-id="62ff9-383">**Quantity:** *5*</span></span>

1. <span data-ttu-id="62ff9-384">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-384">Select **Save**.</span></span>
1. <span data-ttu-id="62ff9-385">På hurtigfanen **Linjedetaljer** på **Oppsett**-fanen noterer du ned verdien for **Parti-ID** for hver linje.</span><span class="sxs-lookup"><span data-stu-id="62ff9-385">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="62ff9-386">Disse verdiene er nødvendige under reservering av bestemte nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="62ff9-386">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62ff9-387">Hvis du vil reservere et bestemt nummerskilt, må du bruke dataenheten **Ordreigangsatte reservasjoner per nummerskilt**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-387">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="62ff9-388">Hvis du vil reservere en partisporet vare på et bestemt nummerskilt, kan du også bruke **Partireservasjon**-siden som beskrevet i delen [Angi salgsordredetaljer](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="62ff9-388">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="62ff9-389">Hvis du angir nummerskiltet direkte på salgsordrelinjen og bekrefter det til systemet, brukes ikke prosessering av lagerstyring for linjen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-389">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="62ff9-390">Velg **Åpne i Microsoft Office**, velg **Ordreigangsatte reservasjoner per nummerskilt**, og last ned filen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-390">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="62ff9-391">Åpne den nedlastede filen i Excel, og velg **Aktiver redigering** for å aktivere kjøring av Excel-tillegget.</span><span class="sxs-lookup"><span data-stu-id="62ff9-391">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="62ff9-392">Hvis du kjører Excel-tillegget for første gang, velger du **Klarer tillegget**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-392">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="62ff9-393">Hvis du blir bedt om å logge på, velger du **Logg på**, og deretter logger du på ved å bruke samme legitimasjon som du brukte til å logge på Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="62ff9-393">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="62ff9-394">Hvis du vil reservere en vare på et bestemt nummerskilt i Excel-tillegget, velger du **Ny** for å legge til en reservasjonslinje, og angir deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="62ff9-394">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="62ff9-395">**Parti-ID:** Angi verdien for **Parti-ID** som du fant for salgsordrelinjen for *Vare 1*.</span><span class="sxs-lookup"><span data-stu-id="62ff9-395">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="62ff9-396">**Nummerskilt:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="62ff9-396">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="62ff9-397">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="62ff9-397">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="62ff9-398">Velg **Ny** for å legge til en ny reservasjonslinje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="62ff9-398">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="62ff9-399">**Parti-ID:** Angi verdien for **Parti-ID** som du fant for salgsordrelinjen for *Vare 2*.</span><span class="sxs-lookup"><span data-stu-id="62ff9-399">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="62ff9-400">**Nummerskilt:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="62ff9-400">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="62ff9-401">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="62ff9-401">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="62ff9-402">I Excel-tillegget velger du **Publiser** for å sende dataene tilbake til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="62ff9-402">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62ff9-403">Reservasjonslinjen vil bare vises i systemet hvis publiseringen er fullført uten feil.</span><span class="sxs-lookup"><span data-stu-id="62ff9-403">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="62ff9-404">Gå tilbake til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="62ff9-404">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="62ff9-405">Hvis du vil gå gjennom varens reservasjon, går du til **Salgsordrelinje**-hurtigfanen på **Lager**-menyen og velger **Vedlikehold \> Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-405">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="62ff9-406">Legg merke til at for salgsordrelinjen for *Vare 1*, er en beholdning på *10* reservert, og for salgsordrelinjen for *Vare 2* er en beholdning på *5* reservert.</span><span class="sxs-lookup"><span data-stu-id="62ff9-406">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="62ff9-407">Hvis du vil se gjennom lagertransaksjoner som er knyttet til salgsordrelinjereservasjonen, går du til **Salgsordrelinjer**-hurtigfanen på **Lager**-menyen og velger **Vis \> Transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-407">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="62ff9-408">Legg merke til at det er to transaksjoner som er knyttet til reserveringen: én der **Referanse**-feltet er satt til *Salgsordre*, og én der **Referanse**-feltet er satt til *Ordreigangsatt reservasjon*.</span><span class="sxs-lookup"><span data-stu-id="62ff9-408">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62ff9-409">En transaksjon der **Referanse**-feltet er satt til *Salgsordre* , representerer ordrelinjereservasjonen for beholdningsdimensjonene som er over **Plassering**-nivået (anlegg, lager og inventarstatus).</span><span class="sxs-lookup"><span data-stu-id="62ff9-409">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="62ff9-410">En transaksjon der **Referanse**-feltet er angitt til *Ordreigangsatt reservasjon*, representerer ordrelinjereservasjonen for det bestemte nummerskiltet og lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-410">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="62ff9-411">Du kan frigi salgsordren ved å gå til handlingsruten og **Lager**-fanen i **Handlinger**-gruppen og velge **Frigi til lager**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-411">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="62ff9-412">Gå gjennom og behandle lagerarbeidet med ordreigangsatte nummerskilt tilordnet</span><span class="sxs-lookup"><span data-stu-id="62ff9-412">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="62ff9-413">På **Salgsordrelinjer**-fanen, på **Lager**-menyen, velger du **Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-413">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="62ff9-414">Når reservasjon er utført for et bestemt parti, bruker ikke systemet lokasjonsdirektiver når det oppretter arbeidet for salgsordren som bruker nummerskiltreservering.</span><span class="sxs-lookup"><span data-stu-id="62ff9-414">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="62ff9-415">Siden den ordreigangsatte reservasjonen angir alle lagerdimensjonene, inkludert lokasjonen, trenger ikke lokasjonsdirektiver å brukes, fordi disse lagerdimensjonene akkurat ble angitt i arbeidet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-415">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="62ff9-416">De vises i delen **Fra lagerdimensjoner** på siden **Arbeidslagertransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-416">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62ff9-417">Etter at arbeidet er opprettet, blir varens beholdningstransaksjon der **Referanse**-feltet er satt til *Ordreigangsatt reservasjon*, fjernet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-417">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="62ff9-418">Beholdningstransaksjonen der **Referanse**-feltet er satt til *Arbeid*, inneholder nå den fysiske reservasjonen for alle beholdningsdimensjoner for antallet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-418">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="62ff9-419">Fullfør plukkingen på mobilenheten, og plasser arbeidet ved hjelp av et menyelement der det er merket av for **Behandle etter nummerskilt**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-419">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62ff9-420">Funksjonaliteten **Behandle etter nummerskilt** hjelper deg med å behandle hele nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-420">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="62ff9-421">Hvis du må behandle deler av nummerskiltet, kan du ikke bruke denne funksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="62ff9-421">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="62ff9-422">Vi anbefaler at du har separat arbeid generert for hvert nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="62ff9-422">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="62ff9-423">Du oppnår dette resultatet ved å bruke funksjonen **Arbeidshodeskift** på **Arbeidsmal**-siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-423">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="62ff9-424">Nummerskiltet *LP02* plukkes nå for salgsordrelinjer og plasseres på *Rampedør*-lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-424">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="62ff9-425">På dette tidspunktet er det klart til å lastes og sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-425">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="62ff9-426">Unntakshåndtering av lagerarbeid som har ordreigangsatte partinumre</span><span class="sxs-lookup"><span data-stu-id="62ff9-426">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="62ff9-427">Lagerarbeid for plukking av ordreigangsatte partinumre er underlagt samme standard lagerunntakshåndtering og -handlinger som vanlig arbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-427">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="62ff9-428">Generelt kan det åpne arbeidet eller arbeidslinjen avbrytes. De kan avbrytes fordi en brukerplassering er full, det kan mangle tilstrekkelig antall, og de kan oppdateres på grunn av en bevegelse.</span><span class="sxs-lookup"><span data-stu-id="62ff9-428">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="62ff9-429">Tilsvarende kan den valgte kvantiteten arbeid som allerede er fullført, reduseres, eller arbeidet kan reverseres.</span><span class="sxs-lookup"><span data-stu-id="62ff9-429">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="62ff9-430">Følgende nøkkelregel brukes for alle disse unntakshåndteringshandlingene: Partinummeret som var reservert for kunden, kan aldri erstattes med et annet partinummer, men lagringsdimensjonene (plassering og nummerskilt) kan endres gjennom enten en manuell oppdatering utført av brukeren eller en automatisk oppdatering utført av systemet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-430">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="62ff9-431">Den automatiske oppdateringen er basert på den samme tilfeldige tilordningen av lagringsdimensjoner som gjaldt da et spesifikt parti ble reservert automatisk, men ingen lagringsdimensjoner ble spesifisert.</span><span class="sxs-lookup"><span data-stu-id="62ff9-431">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="62ff9-432">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="62ff9-432">Example scenario</span></span>

<span data-ttu-id="62ff9-433">Et eksempel på dette scenarioet er en situasjon der tidligere avsluttet arbeid plukkes fra hverandre ved å benytte **Reduser plukket kvantitet**-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-433">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="62ff9-434">Dette eksemplet forutsetter at du allerede har fullført trinnene som er beskrevet i [Eksempelscenario: Tildeling av partinummer](#Example-batch-allocation).</span><span class="sxs-lookup"><span data-stu-id="62ff9-434">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="62ff9-435">Den fortsetter fra dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-435">It continues from that example.</span></span>

1. <span data-ttu-id="62ff9-436">Gå til **Lagerstyring** \> **Belastninger** \> **Aktive belastninger**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-436">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="62ff9-437">Velg belastningen som ble opprettet i forbindelse med forsendelsen av salgsordren.</span><span class="sxs-lookup"><span data-stu-id="62ff9-437">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="62ff9-438">Gå til **Last inn ordrelinjer**-hurtigfanen og velg **Reduser plukket kvantitet**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-438">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="62ff9-439">Gå til **Reduser plukket kvantitet**-siden i **Flytt til plassering**-feltet og velg **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-439">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="62ff9-440">I **Flytt til nummerskilt**-feltet velger du **LP33**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-440">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="62ff9-441">I rutenettet, i **Beholdningskvantitet som skal plukkes vekk**-feltet, angir du **10**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-441">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="62ff9-442">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-442">Select **OK**.</span></span>

<span data-ttu-id="62ff9-443">Her er resultatene av handlingen med vekkplukking:</span><span class="sxs-lookup"><span data-stu-id="62ff9-443">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="62ff9-444">Statusen til det tidligere lukkede verket er satt til **Avbrutt**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-444">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="62ff9-445">Nytt arbeid av **Beholdningsbevegelse**-typen opprettes for det vekkplukkede antallet **10** for partinummer **B11**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-445">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="62ff9-446">Dette arbeidet representerer bevegelsen fra **Båsdør**-plasseringen til nummerskiltet **LP33** på plasseringen **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-446">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="62ff9-447">Status er satt til **Lukket**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-447">The status is set to **Closed**.</span></span>
- <span data-ttu-id="62ff9-448">Systemet reserverer partinummeret som opprinnelig ble bestilt, på nytt og tilordner plasseringen og nummerskilt-ID-er.</span><span class="sxs-lookup"><span data-stu-id="62ff9-448">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="62ff9-449">(Denne prosessen tilsvarer kjøring av **Reserver linje**-funksjonen for ordrelinjen for et gitt partinummer).</span><span class="sxs-lookup"><span data-stu-id="62ff9-449">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="62ff9-450">Som et resultat vises parti **B11** som bundet på **Partinumre bundet til kildelinje**-hurtigfanen på **Partireservasjon**-siden, og **Reservasjon**-feltet inneholder antallet **10** for partinummer **B11**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-450">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="62ff9-451">I tillegg er **Plassering**-feltet satt til **FL-001**, og **Nummerskilt**-feltet er satt til **LP11**.</span><span class="sxs-lookup"><span data-stu-id="62ff9-451">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="62ff9-452">(Du kan legge til disse feltene i rutenettet hvis de ikke er synlige.)</span><span class="sxs-lookup"><span data-stu-id="62ff9-452">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="62ff9-453">Følgende tabeller inneholder en oversikt som viser hvordan systemet håndterer ordreigangsatt partireservasjon for bestemte lagerhandlinger.</span><span class="sxs-lookup"><span data-stu-id="62ff9-453">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="62ff9-454">Hvis du vil tolke innholdet i tabellene, må du anta at hver lagerhandling kjøres i konteksten av eksisterende lagerarbeid som stammer fra en ordreigangsatt partireservasjon, eller at utførelsen av hver lagerhandling påvirker arbeid av denne typen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-454">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="62ff9-455">I disse tabellene angir "Partikvantitet er tilgjengelig"-kolonnen om en partikvantitet er tilgjengelig, i tillegg til kvantiteten som allerede er reservert for gjeldende ordreigangsatte reservasjoner, eller som allerede er reservert av lagerarbeidet som stammer fra reservasjoner av denne typen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-455">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="62ff9-456">Overstyr plukkplasseringen for det åpne arbeidet</span><span class="sxs-lookup"><span data-stu-id="62ff9-456">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="62ff9-457">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="62ff9-457">Key setup parameter</span></span></th>
<th><span data-ttu-id="62ff9-458">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="62ff9-458">Batch quantity is available</span></span></th>
<th><span data-ttu-id="62ff9-459">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="62ff9-459">Key user steps</span></span></th>
<th><span data-ttu-id="62ff9-460">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="62ff9-460">Warehouse work</span></span></th>
<th><span data-ttu-id="62ff9-461">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="62ff9-461">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="62ff9-462"><strong>Tillat overstyring av plukkplassering</strong>-alternativet er aktivert for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="62ff9-462">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="62ff9-463">Ja</span><span class="sxs-lookup"><span data-stu-id="62ff9-463">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-464">Velg <strong>Overstyr plassering</strong>-menyelementet på lagerappen når du begynner plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-464">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="62ff9-465">Velg <strong>Foreslå</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-465">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="62ff9-466">Bekreft den nye plasseringen som foreslås, basert på tilgjengeligheten av partikvantitet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-466">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="62ff9-467">For gjeldende arbeid oppstår det følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="62ff9-467">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="62ff9-468">Plasseringen på plukklinjen oppdateres til den nye plasseringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-468">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="62ff9-469">(Hvis plasseringen er navneskiltstyrt, tilordnes et tilfeldig nummerskilt til arbeidslagertransaksjonen, og arbeideren kan plukke et hvilket som helst nummerskilt som har tilgjengelig kvantitet.)</span><span class="sxs-lookup"><span data-stu-id="62ff9-469">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="62ff9-470">Hvis kvantiteten blir funnet for mer enn ett nummerskilt på den nye plasseringen, blir den opprinnelige plukklinjen delt opp i flere linjer for å matche hvert nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="62ff9-470">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="62ff9-471">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-471">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-472">Nr.</span><span class="sxs-lookup"><span data-stu-id="62ff9-472">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-473">Velg <strong>Overstyr plassering</strong>-menyelementet på lagerappen når du begynner plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-473">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="62ff9-474">Angi en plassering manuelt.</span><span class="sxs-lookup"><span data-stu-id="62ff9-474">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="62ff9-475"><strong>Overstyr plassering</strong>-handlingen er ikke mulig.</span><span class="sxs-lookup"><span data-stu-id="62ff9-475">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="62ff9-476">Den mislykkes, og det oppstår en feil.</span><span class="sxs-lookup"><span data-stu-id="62ff9-476">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="62ff9-477">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-477">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="62ff9-478">Full knapp – del opp en arbeidslinje på grunn av overflyt på brukerplasseringen</span><span class="sxs-lookup"><span data-stu-id="62ff9-478">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="62ff9-479">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="62ff9-479">Key setup parameter</span></span></th>
<th><span data-ttu-id="62ff9-480">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="62ff9-480">Batch quantity is available</span></span></th>
<th><span data-ttu-id="62ff9-481">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="62ff9-481">Key user steps</span></span></th>
<th><span data-ttu-id="62ff9-482">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="62ff9-482">Warehouse work</span></span></th>
<th><span data-ttu-id="62ff9-483">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="62ff9-483">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="62ff9-484"><strong>Tillat oppdeling av arbeid</strong>-alternativet er aktivert på mobilenhetens menyelement.</span><span class="sxs-lookup"><span data-stu-id="62ff9-484">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="62ff9-485">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-485">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-486">Velg menyelementet <strong>Full</strong> på lagerappen når du behandler plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-486">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="62ff9-487">I <strong>Plukkvantitet</strong>-feltet angir du en delvis kvantitet for den påkrevde plukkingen for å indikere hele kapasiteten.</span><span class="sxs-lookup"><span data-stu-id="62ff9-487">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="62ff9-488">I gjeldende arbeid oppdateres kvantiteten til den gjenværende kvantiteten som må plukkes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-488">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="62ff9-489">Nytt arbeid for den plukkede kvantiteten opprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-489">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="62ff9-490">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-490">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="62ff9-491">Redusere den plukkede kvantiteten for fullført arbeid (fra en belastning)</span><span class="sxs-lookup"><span data-stu-id="62ff9-491">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="62ff9-492">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="62ff9-492">Key setup parameter</span></span></th>
<th><span data-ttu-id="62ff9-493">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="62ff9-493">Batch quantity is available</span></span></th>
<th><span data-ttu-id="62ff9-494">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="62ff9-494">Key user steps</span></span></th>
<th><span data-ttu-id="62ff9-495">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="62ff9-495">Warehouse work</span></span></th>
<th><span data-ttu-id="62ff9-496">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="62ff9-496">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="62ff9-497">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-497">Not applicable</span></span></td>
<td><span data-ttu-id="62ff9-498">Ja</span><span class="sxs-lookup"><span data-stu-id="62ff9-498">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-499">Åpne <strong>Reduser plukket kvantitet</strong>-siden fra belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-499">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="62ff9-500">Angi den fullstendige kvantiteten som skal plukkes vekk.</span><span class="sxs-lookup"><span data-stu-id="62ff9-500">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="62ff9-501">Velg "Flytt til"-plassering/-nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="62ff9-501">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="62ff9-502">Arbeid som er knyttet til belastningslinjen, avbrytes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-502">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="62ff9-503">Nytt arbeid for beholdningsbevegelsen opprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-503">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="62ff9-504">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-504">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="62ff9-505">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="62ff9-505">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-506">Nei</span><span class="sxs-lookup"><span data-stu-id="62ff9-506">No</span></span></td>
<td><span data-ttu-id="62ff9-507">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-507">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-508">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-508">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-509">Kvantiteten reserveres på nytt for samme parti, samt for samme plassering og nummerskilt (hvis plasseringen er nummerskiltstyrt) som ble angitt under vekkplukking.</span><span class="sxs-lookup"><span data-stu-id="62ff9-509">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="62ff9-510">Flytte en vare i et lager</span><span class="sxs-lookup"><span data-stu-id="62ff9-510">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="62ff9-511">Denne lagerhandlingen gjelder bare for bevegelse av **Arbeidsopprettelsesprosess**-typen, ikke for bevegelse etter mal.</span><span class="sxs-lookup"><span data-stu-id="62ff9-511">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="62ff9-512">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="62ff9-512">Key setup parameter</span></span></th>
<th><span data-ttu-id="62ff9-513">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="62ff9-513">Batch quantity is available</span></span></th>
<th><span data-ttu-id="62ff9-514">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="62ff9-514">Key user steps</span></span></th>
<th><span data-ttu-id="62ff9-515">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="62ff9-515">Warehouse work</span></span></th>
<th><span data-ttu-id="62ff9-516">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="62ff9-516">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="62ff9-517"><strong>Tillat bevegelse av beholdning med tilhørende arbeid</strong>-alternativet er aktivert for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="62ff9-517">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="62ff9-518">Ja</span><span class="sxs-lookup"><span data-stu-id="62ff9-518">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-519">Start en flytting på lagerappen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-519">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="62ff9-520">Angi "fra"- og "til"-plasseringene.</span><span class="sxs-lookup"><span data-stu-id="62ff9-520">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="62ff9-521">For alt eksisterende arbeid som påvirkes av flyttingen, oppdateres plukkplasseringen til den nye plasseringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-521">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="62ff9-522">Nytt arbeid for beholdningsbevegelsen opprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-522">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="62ff9-523">Alle eksisterende reservasjoner som påvirkes av kvantitetsbevegelsen fra den gitte plasseringen, reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-523">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="62ff9-524">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="62ff9-524">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-525">Nei</span><span class="sxs-lookup"><span data-stu-id="62ff9-525">No</span></span></td>
<td><span data-ttu-id="62ff9-526">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-526">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-527">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-527">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-528">Alle eksisterende reservasjoner som påvirkes av kvantitetsbevegelsen fra den gitte plasseringen, reserveres for samme parti, samt for den nye "til"- plasseringen og det nye "til"-nummerskiltet (hvis plasseringen er nummerskiltstyrt).</span><span class="sxs-lookup"><span data-stu-id="62ff9-528">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="62ff9-529">Reversere den plukkede kvantiteten for fullført arbeid (fra en belastning eller en bølge)</span><span class="sxs-lookup"><span data-stu-id="62ff9-529">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="62ff9-530">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="62ff9-530">Key setup parameter</span></span></th>
<th><span data-ttu-id="62ff9-531">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="62ff9-531">Batch quantity is available</span></span></th>
<th><span data-ttu-id="62ff9-532">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="62ff9-532">Key user steps</span></span></th>
<th><span data-ttu-id="62ff9-533">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="62ff9-533">Warehouse work</span></span></th>
<th><span data-ttu-id="62ff9-534">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="62ff9-534">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="62ff9-535">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-535">Not applicable</span></span></td>
<td><span data-ttu-id="62ff9-536">Ja</span><span class="sxs-lookup"><span data-stu-id="62ff9-536">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-537">Åpne <strong>Reverser arbeid</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-537">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="62ff9-538">På forespørselssiden velger du <strong>Etterlat varer på gjeldende plassering</strong>-alternativet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-538">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="62ff9-539">Alt arbeid som er knyttet til belastningen, avbrytes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-539">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="62ff9-540">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-540">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="62ff9-541">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="62ff9-541">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-542">Nei</span><span class="sxs-lookup"><span data-stu-id="62ff9-542">No</span></span></td>
<td><span data-ttu-id="62ff9-543">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-543">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-544">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-544">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-545">Kvantiteten reserveres på nytt for samme parti, samt for plasseringen og nummerskiltet der kvantiteten ble etterlatt ved reversering.</span><span class="sxs-lookup"><span data-stu-id="62ff9-545">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-546">Ja</span><span class="sxs-lookup"><span data-stu-id="62ff9-546">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-547">Åpne <strong>Reverser arbeid</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-547">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="62ff9-548">På forespørselssiden velger du <strong>Tilordne varer til denne plasseringen</strong>-alternativet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-548">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="62ff9-549">Det gjeldende arbeidet avbrytes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-549">The current work is canceled.</span></span></li>
<li><span data-ttu-id="62ff9-550">Nytt arbeid for beholdningsbevegelsen opprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-550">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="62ff9-551">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-551">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="62ff9-552">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="62ff9-552">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-553">Nei</span><span class="sxs-lookup"><span data-stu-id="62ff9-553">No</span></span></td>
<td><span data-ttu-id="62ff9-554">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-554">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-555">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-555">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-556">Kvantiteten reserveres på nytt for samme parti, samt for plasseringen og nummerskiltet som kvantiteten ble tilordnet til ved reversering.</span><span class="sxs-lookup"><span data-stu-id="62ff9-556">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-557">Ja/nei</span><span class="sxs-lookup"><span data-stu-id="62ff9-557">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-558">Åpne <strong>Reverser arbeid</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-558">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="62ff9-559">På forespørselssiden velger du <strong>Flytt varer til denne plasseringen</strong>-alternativet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-559">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="62ff9-560">Reversering støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="62ff9-560">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="62ff9-561">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-561">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-562">Ja/nei</span><span class="sxs-lookup"><span data-stu-id="62ff9-562">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-563">Åpne <strong>Reverser arbeid</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-563">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="62ff9-564">På forespørselssiden velger du <strong>Flytt varer basert på plasseringsdirektiver</strong>-alternativet.</span><span class="sxs-lookup"><span data-stu-id="62ff9-564">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="62ff9-565">Reversering støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="62ff9-565">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="62ff9-566">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-566">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="62ff9-567">Plukk en kvantitet med mangler – Registrer kvantiteten som fysisk ikke funnet på plasseringen/nummerskiltet mens du utfører plukkarbeidet</span><span class="sxs-lookup"><span data-stu-id="62ff9-567">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="62ff9-568">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="62ff9-568">Key setup parameter</span></span></th>
<th><span data-ttu-id="62ff9-569">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="62ff9-569">Batch quantity is available</span></span></th>
<th><span data-ttu-id="62ff9-570">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="62ff9-570">Key user steps</span></span></th>
<th><span data-ttu-id="62ff9-571">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="62ff9-571">Warehouse work</span></span></th>
<th><span data-ttu-id="62ff9-572">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="62ff9-572">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="62ff9-573">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Ingen</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-573">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="62ff9-574">Ja</span><span class="sxs-lookup"><span data-stu-id="62ff9-574">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-575">Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-575">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="62ff9-576">I feltet <strong>Plukkekvantitet</strong> angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="62ff9-576">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="62ff9-577">I <strong>Årsak</strong>-feltet angir du <strong>Ingen ny fordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-577">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="62ff9-578">Gjeldende arbeid lukkes, og den plukkede kvantiteten er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="62ff9-578">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="62ff9-579">Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-579">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="62ff9-580">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-580">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="62ff9-581">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="62ff9-581">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-582">Nei</span><span class="sxs-lookup"><span data-stu-id="62ff9-582">No</span></span></td>
<td><span data-ttu-id="62ff9-583">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-583">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="62ff9-584">Handlingen for plukking med mangler mislykkes, og det oppstår en feil.</span><span class="sxs-lookup"><span data-stu-id="62ff9-584">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="62ff9-585">Gjeldende arbeid forblir åpent.</span><span class="sxs-lookup"><span data-stu-id="62ff9-585">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="62ff9-586">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-586">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="62ff9-587">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Ingen</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-587">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="62ff9-588">Ja</span><span class="sxs-lookup"><span data-stu-id="62ff9-588">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-589">Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-589">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="62ff9-590">I feltet <strong>Plukkekvantitet</strong> angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="62ff9-590">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="62ff9-591">I <strong>Årsak</strong>-feltet angir du <strong>Ingen ny fordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-591">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="62ff9-592">Gjeldende arbeid lukkes, og den plukkede kvantiteten er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="62ff9-592">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="62ff9-593">Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-593">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="62ff9-594">Alle eksisterende reservasjoner som påvirkes av kvantitetsjusteringen i plasseringen for plukking med mangler, reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-594">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="62ff9-595">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="62ff9-595">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-596">Nei</span><span class="sxs-lookup"><span data-stu-id="62ff9-596">No</span></span></td>
<td><span data-ttu-id="62ff9-597">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-597">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-598">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-598">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-599">Alle eksisterende reservasjoner som påvirkes av kvantitetsjusteringen i plasseringen for plukking med mangler, fjernes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-599">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-600">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Manuell</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Nei/Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-600">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="62ff9-601">I tillegg er <strong>Tillat manuell omfordeling av varer</strong>-alternativet aktivert for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="62ff9-601">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="62ff9-602">Ja</span><span class="sxs-lookup"><span data-stu-id="62ff9-602">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-603">Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-603">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="62ff9-604">I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="62ff9-604">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="62ff9-605">I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med manuell omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-605">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="62ff9-606">Velg plasseringen/nummerskiltet i listen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-606">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="62ff9-607">For gjeldende arbeid oppstår det følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="62ff9-607">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="62ff9-608">Plukklinjen lukkes, og den plukkede kvantiteten er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="62ff9-608">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="62ff9-609">Plasseringslinjen avbrytes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-609">The put line is canceled.</span></span></li>
<li><span data-ttu-id="62ff9-610">Det opprettes en ny plukklinje.</span><span class="sxs-lookup"><span data-stu-id="62ff9-610">A new pick line is created.</span></span> <span data-ttu-id="62ff9-611">Den bruker plasseringen/nummerskiltet som brukeren valgte.</span><span class="sxs-lookup"><span data-stu-id="62ff9-611">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="62ff9-612">Det opprettes en ny plasseringslinje.</span><span class="sxs-lookup"><span data-stu-id="62ff9-612">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="62ff9-613">Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-613">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="62ff9-614">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-614">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-615">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Manuell</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-615">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="62ff9-616">I tillegg er <strong>Tillat manuell omfordeling av varer</strong>-alternativet aktivert for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="62ff9-616">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="62ff9-617">Nr.</span><span class="sxs-lookup"><span data-stu-id="62ff9-617">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-618">Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-618">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="62ff9-619">I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="62ff9-619">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="62ff9-620">I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med manuell omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-620">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="62ff9-621">Handlingen for plukking med mangler mislykkes, og det oppstår en feil.</span><span class="sxs-lookup"><span data-stu-id="62ff9-621">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="62ff9-622">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-622">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-623">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Manuell</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-623">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="62ff9-624">I tillegg er <strong>Tillat manuell omfordeling av varer</strong>-alternativet aktivert for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="62ff9-624">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="62ff9-625">Nr.</span><span class="sxs-lookup"><span data-stu-id="62ff9-625">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-626">Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-626">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="62ff9-627">I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="62ff9-627">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="62ff9-628">I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med manuell omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-628">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="62ff9-629">Velg plasseringen/nummerskiltet i listen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-629">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="62ff9-630">For gjeldende arbeid oppstår det følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="62ff9-630">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="62ff9-631">Plukklinjen lukkes, og den plukkede kvantiteten er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="62ff9-631">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="62ff9-632">Plasseringslinjen avbrytes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-632">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="62ff9-633">Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-633">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="62ff9-634">Alle eksisterende reservasjoner som påvirkes av kvantitetsjusteringen i plasseringen/nummerskiltet for plukking med mangler, fjernes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-634">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-635">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Automatisk</strong>, <strong>Juster beholdning</strong> = <strong>Ja/Nei</strong> og <strong>Fjern reservasjoner</strong> = <strong>Ja/Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-635">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="62ff9-636">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="62ff9-636">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-637">Velg <strong>Plukk med mangler</strong>-menyelementet på lagerappen når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-637">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="62ff9-638">I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="62ff9-638">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="62ff9-639">I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med automatisk omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-639">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="62ff9-640">Plukking med mangler som involverer automatisk omfordeling, støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="62ff9-640">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="62ff9-641">Plukking med mangler som involverer automatisk omfordeling, støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="62ff9-641">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="62ff9-642">Endre beholdningsstatusen</span><span class="sxs-lookup"><span data-stu-id="62ff9-642">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="62ff9-643">Denne lagerhandlingen kan utføres fra flere inngangspunkter.</span><span class="sxs-lookup"><span data-stu-id="62ff9-643">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="62ff9-644">I eksempelet som vises her, benyttes **Beholdningsstatusendring**-handlingen på **På lager etter plassering**-siden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-644">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="62ff9-645">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="62ff9-645">Key setup parameter</span></span></th>
<th><span data-ttu-id="62ff9-646">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="62ff9-646">Batch quantity is available</span></span></th>
<th><span data-ttu-id="62ff9-647">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="62ff9-647">Key user steps</span></span></th>
<th><span data-ttu-id="62ff9-648">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="62ff9-648">Warehouse work</span></span></th>
<th><span data-ttu-id="62ff9-649">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="62ff9-649">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="62ff9-650">I <strong>Lager</strong>-fanen, i <strong>Lager</strong>-oppføringen, er <strong>Fjern reservasjoner og merkinger</strong>-feltet satt til <strong>Reservasjoner</strong> eller <strong>Merkinger og reservasjoner</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-650">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="62ff9-651">Ja</span><span class="sxs-lookup"><span data-stu-id="62ff9-651">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-652">Velg en spesifikk plassering.</span><span class="sxs-lookup"><span data-stu-id="62ff9-652">Select a specific location.</span></span></li>
<li><span data-ttu-id="62ff9-653">Velg en linje som har et spesifikt element, en spesifikk plassering og et spesifikt nummerskilt (hvis plasseringen er nummerskiltstyrt).</span><span class="sxs-lookup"><span data-stu-id="62ff9-653">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="62ff9-654">Velg <strong>Beholdningsstatusendring</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-654">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="62ff9-655">Sett <strong>Beholdningsstatus</strong>-feltet til <strong>Blokkering</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-655">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="62ff9-656">Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-656">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="62ff9-657">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-657">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="62ff9-658">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="62ff9-658">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="62ff9-659">Det opprettes to beholdningstransaksjoner av <strong>Beholdningsstatusendring</strong>-typen for å representere endringen i beholdningsstatusdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-659">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="62ff9-660">En beholdningstransaksjon av <strong>Beholdningsblokkering</strong>-typen og <strong>Reservert fysisk</strong>-utstedelsestypen opprettes for å representere reservasjonen av den blokkerte kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="62ff9-660">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-661">Nei</span><span class="sxs-lookup"><span data-stu-id="62ff9-661">No</span></span></td>
<td><span data-ttu-id="62ff9-662">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-662">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-663">Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-663">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="62ff9-664">Reservasjonen fjernes.</span><span class="sxs-lookup"><span data-stu-id="62ff9-664">The reservation is removed.</span></span></li>
<li><span data-ttu-id="62ff9-665">Det opprettes to beholdningstransaksjoner av <strong>Beholdningsstatusendring</strong>-typen for å representere endringen i beholdningsstatusdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="62ff9-665">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="62ff9-666">En beholdningstransaksjon av <strong>Beholdningsblokkering</strong>-typen og <strong>Reservert fysisk</strong>-utstedelsestypen opprettes for å representere reservasjonen av den blokkerte kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="62ff9-666">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="62ff9-667">I <strong>Lager</strong>-fanen, i <strong>Lager</strong>-oppføringen, er <strong>Fjern reservasjoner og merkinger</strong>-feltet satt til <strong>Ingen</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-667">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="62ff9-668">Ja</span><span class="sxs-lookup"><span data-stu-id="62ff9-668">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="62ff9-669">Velg en spesifikk plassering.</span><span class="sxs-lookup"><span data-stu-id="62ff9-669">Select a specific location.</span></span></li>
<li><span data-ttu-id="62ff9-670">Velg en linje som har et spesifikt element, en spesifikk plassering og et spesifikt nummerskilt (hvis plasseringen er nummerskiltstyrt).</span><span class="sxs-lookup"><span data-stu-id="62ff9-670">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="62ff9-671">Velg <strong>Beholdningsstatusendring</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-671">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="62ff9-672">Sett <strong>Beholdningsstatus</strong>-feltet til <strong>Blokkering</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ff9-672">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="62ff9-673">Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-673">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="62ff9-674">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="62ff9-674">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="62ff9-675">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="62ff9-675">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="62ff9-676">Nei</span><span class="sxs-lookup"><span data-stu-id="62ff9-676">No</span></span></td>
<td><span data-ttu-id="62ff9-677">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="62ff9-677">See the previous row.</span></span></td>
<td><span data-ttu-id="62ff9-678">Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-678">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="62ff9-679">Beholdningsstatusendringer er ikke tillatt.</span><span class="sxs-lookup"><span data-stu-id="62ff9-679">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="62ff9-680">Begrensninger</span><span class="sxs-lookup"><span data-stu-id="62ff9-680">Limitations</span></span>

- <span data-ttu-id="62ff9-681">Den fleksible funksjonaliteten for dimensjonsreservasjon på lagernivå støtter ikke følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="62ff9-681">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="62ff9-682">Administrering av faktisk vekt</span><span class="sxs-lookup"><span data-stu-id="62ff9-682">Catch weight management</span></span>
    - <span data-ttu-id="62ff9-683">Fysisk negativt lager</span><span class="sxs-lookup"><span data-stu-id="62ff9-683">Physical negative inventory</span></span>
    - <span data-ttu-id="62ff9-684">Reservasjon mot bestilt forsyning</span><span class="sxs-lookup"><span data-stu-id="62ff9-684">Reservation against ordered supply</span></span>
    - <span data-ttu-id="62ff9-685">Plukking av overføringsordrer og råvarer</span><span class="sxs-lookup"><span data-stu-id="62ff9-685">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="62ff9-686">Regelen for konsolidering av containere for pakking etter direktivenhet har begrensninger.</span><span class="sxs-lookup"><span data-stu-id="62ff9-686">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="62ff9-687">For ordreigangsatte reservasjoner anbefaler vi at du ikke bruker maler for containerbygging i tilfeller der **Pakk etter direktivenhet**-feltet er aktivert.</span><span class="sxs-lookup"><span data-stu-id="62ff9-687">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="62ff9-688">I gjeldende utforming brukes ikke plasseringsdirektiver når det opprettes lagerarbeid.</span><span class="sxs-lookup"><span data-stu-id="62ff9-688">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="62ff9-689">Derfor brukes bare den laveste enheten i enhetssekvensgruppen (beholdningsenheten) under bølgetrinnet containerbruk.</span><span class="sxs-lookup"><span data-stu-id="62ff9-689">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
