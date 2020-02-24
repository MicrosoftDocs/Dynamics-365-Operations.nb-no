---
title: Fleksibel retningslinje for dimensjonsreservasjon på lagernivå
description: Dette emnet beskriver retningslinjen for beholdningsreservasjon som lar virksomheter som selger partisporede produkter og kjører logistikken som WMS-aktiverte operasjoner, reservere spesifikke partier for kundesalgsordrer, selv om reservasjonshierarkiet som er assosiert med produktene, ikke tillater reservasjon av spesifikke partier.
author: omulvad
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c0baf96315dd9fe6bc1984d337fd1c50ae47016a
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031049"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="64a6b-103">Fleksibel retningslinje for dimensjonsreservasjon på lagernivå</span><span class="sxs-lookup"><span data-stu-id="64a6b-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64a6b-104">Når et hierarki for beholdningsreservasjon av "Parti under\[plassering\]"-typen er assosiert med produkter, kan bedrifter som selger partisporede produkter og kjører logistikken som operasjoner som er aktivert for Microsoft Dynamics 365 Warehouse Management System (WMS), ikke reservere spesifikke partier av disse produktene for kundesalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="64a6b-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="64a6b-105">Dette emnet beskriver retningslinjen for beholdningsreservasjon som lar disse virksomhetene reservere spesifikke partier, selv når produktene er assosiert med et "Parti under\[plassering\]"-reservasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="64a6b-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="64a6b-106">Beholdningsreservasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="64a6b-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="64a6b-107">Dette avsnittet oppsummerer det eksisterende beholdningsreservasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="64a6b-108">Det fokuserer på måten partisporede og seriesporede varer håndteres på.</span><span class="sxs-lookup"><span data-stu-id="64a6b-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="64a6b-109">Beholdningsreservasjonshierarkiet dikterer følgende: For lagringsdimensjoner angir etterspørselsordren de obligatoriske dimensjonene for sted, lager og beholdningsstatus, mens lagerlogikken har ansvar for å tilordne et sted til de forespurte kvantitetene og for å reservere stedet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="64a6b-110">Med andre ord gjelder følgende: I samhandlingene mellom etterspørselsordren og lagervirksomheten, forventes etterspørselsordren å indikere hvor ordren må sendes fra (det vil si hvilket sted og lager).</span><span class="sxs-lookup"><span data-stu-id="64a6b-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="64a6b-111">Lageret er deretter avhengig av logikken for å finne påkrevd kvantitet i lagerlokalene.</span><span class="sxs-lookup"><span data-stu-id="64a6b-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="64a6b-112">For å gjenspeile virksomhetens driftsmodell er sporingsdimensjoner (parti- og serienumre) imidlertid gjenstand for mer fleksibilitet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="64a6b-113">Et beholdningsreservasjonshierarki kan omfatte scenarioer der følgende betingelser gjelder:</span><span class="sxs-lookup"><span data-stu-id="64a6b-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="64a6b-114">Virksomheten avhenger av lagervirksomheten når det gjelder administrering av plukking av kvantiteter som har parti- eller serienumre, etter at kvantitetene er funnet i lagerlokalene.</span><span class="sxs-lookup"><span data-stu-id="64a6b-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="64a6b-115">Denne modellen henvises ofte til som *Parti under\[plassering\]*.</span><span class="sxs-lookup"><span data-stu-id="64a6b-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="64a6b-116">Den brukes vanligvis når et produkts parti- eller serienummeridentifikasjon ikke er viktig for kundene som legger inn etterspørselen hos det selgende selskapet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="64a6b-117">Hvis parti- eller serienumre er en del av en kundes ordrespesifikasjon, og de registreres i etterspørselsordren, blir lageroperasjonene som finner kvantitetene på lageret, begrenset av de spesifikke forespurte numrene og har ikke lov til å endre dem.</span><span class="sxs-lookup"><span data-stu-id="64a6b-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="64a6b-118">Denne modellen henvises til som *Parti over\[plassering\]*.</span><span class="sxs-lookup"><span data-stu-id="64a6b-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="64a6b-119">I disse scenarioene er utfordringen at bare ett beholdningsreservasjonshierarki kan tilordnes til hvert utgitte produkt.</span><span class="sxs-lookup"><span data-stu-id="64a6b-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="64a6b-120">For at WMS skal kunne håndtere sporede elementer gjelder derfor følgende: Etter at hierarkitildelingen bestemmer når parti- eller serienummeret skal reserveres (enten når etterspørselsordren tas imot eller under lagerplukkearbeidet), kan denne timingen ikke endres på et ad hoc-grunnlag.</span><span class="sxs-lookup"><span data-stu-id="64a6b-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="64a6b-121">Fleksibel reservasjon for partisporede varer</span><span class="sxs-lookup"><span data-stu-id="64a6b-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="64a6b-122">Forretningsscenario</span><span class="sxs-lookup"><span data-stu-id="64a6b-122">Business scenario</span></span>

<span data-ttu-id="64a6b-123">I dette scenarioet bruker et selskap en beholdningsstrategi der fullførte varer spores etter partinumre.</span><span class="sxs-lookup"><span data-stu-id="64a6b-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="64a6b-124">Dette selskapet bruker også WHS-arbeidsbelastning.</span><span class="sxs-lookup"><span data-stu-id="64a6b-124">This company also uses the WHS workload.</span></span> <span data-ttu-id="64a6b-125">Fordi denne arbeidsbelastningen har velutstyrt logikk for planlegging og drift av lagerplukkings- og forsendelsesoperasjoner for partiaktiverte varer, er de fleste av de fullførte varene tilknyttet et "Parti under\[plassering\]"-beholdningsreservasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="64a6b-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="64a6b-126">Fordelen med denne typen driftsoppsett er at beslutninger (som faktisk er reservasjonsbeslutninger) om hvilke partier du skal plukkes, og hvor de skal settes på lageret, utsettes til lagerplukkingsoperasjonene starter.</span><span class="sxs-lookup"><span data-stu-id="64a6b-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="64a6b-127">De utføres ikke når kundens ordre legges inn.</span><span class="sxs-lookup"><span data-stu-id="64a6b-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="64a6b-128">Selv om "Parti under\[plassering\]"-reservasjonshierarkiet tjener selskapets forretningsmessige mål godt, krever mange av selskapets etablerte kunder det samme partiet som de kjøpte tidligere, når de bestiller produkter på nytt.</span><span class="sxs-lookup"><span data-stu-id="64a6b-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="64a6b-129">Derfor leter selskapet etter fleksibilitet i måten partireservasjonsreglene håndteres på, slik at det – avhengig av kundenes etterspørsel etter samme vare – oppstår følgende atferd:</span><span class="sxs-lookup"><span data-stu-id="64a6b-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="64a6b-130">Et partinummer kan registreres og reserveres når ordren tas imot av salgsprosessoren, og det kan ikke endres under lageroperasjoner og/eller tas imot av andre krav.</span><span class="sxs-lookup"><span data-stu-id="64a6b-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="64a6b-131">Denne atferden er med på å garantere at partinummeret som ble bestilt, sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="64a6b-132">Hvis partinummeret ikke er viktig for kunden, kan lageroperasjonen bestemme et partinummer under plukkearbeid, etter at salgsordreregistrering og reservasjon er utført.</span><span class="sxs-lookup"><span data-stu-id="64a6b-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="64a6b-133">Tillate reservering av et bestemt parti i salgsordren</span><span class="sxs-lookup"><span data-stu-id="64a6b-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="64a6b-134">For å imøtekomme ønsket fleksibilitet i partireservasjonsatferden for varer som er assosiert med et "Parti under\[plassering\]"-beholdningsreservasjonshierarki, må beholdningsledere merke av i **Tillat reservasjon på etterspørselsordre**-avmerkingsboksen for **Partinummer**-nivået på **Beholdningsreservasjonshierarkier**-siden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Gjøre beholdningsreservasjonshierarkiet fleksibelt](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="64a6b-136">Når **Partinummer**-nivået i hierarkiet er valgt, vil alle dimensjoner over det nivået og opp gjennom **Plassering**-nivået valgt automatisk.</span><span class="sxs-lookup"><span data-stu-id="64a6b-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="64a6b-137">(Som standard er alle dimensjoner over **Plassering**-nivået forhåndsvalgt.) Denne atferden gjenspeiler logikken der alle dimensjoner i området mellom partinummeret og plasseringen også reserveres automatisk etter at du har reservert et spesifikt partinummer på ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="64a6b-138">**Tillat reservasjon på etterspørselsordre**-avmerkingsboksen gjelder bare for reservasjonshierarkinivåer som er under dimensjonen til lagerplasseringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="64a6b-139">**Partinummer** er det eneste nivået i hierarkiet som er åpent for den fleksible reservasjonsretningslinjen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="64a6b-140">Med andre ord kan du ikke merke av i **Tillat reservasjon på etterspørselsordre**-avmerkingsboksen for **Plassering**-, **Nummerskilt**- eller **Serienummer**-nivået.</span><span class="sxs-lookup"><span data-stu-id="64a6b-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="64a6b-141">Hvis reservasjonshierarkiet inkluderer serienummerdimensjonen (som alltid må være under **Partinummer**-nivået), og hvis du har aktivert partispesifikk reservasjon for partinummeret, vil systemet fortsette å håndtere serienummerreservasjon og plukkeoperasjoner, basert på reglene som gjelder for "Serienr. under\[plassering\]"-reservasjonsretningslinjen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="64a6b-142">Du kan når som helst tillate partispesifikk reservasjon for et eksisterende "Parti under\[plassering\]"-reservasjonshierarki i distribusjonen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="64a6b-143">Denne endringen påvirker ikke reservasjoner og åpent lagerarbeid som ble opprettet før endringen fant sted.</span><span class="sxs-lookup"><span data-stu-id="64a6b-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="64a6b-144">**Tillat reservasjon på etterspørselsordre**-avmerkingsboksen kan imidlertid ikke tømmes hvis det finnes beholdningstransaksjoner med utstedelsestypen **Reservert bestilt**, **Reservert fysisk** eller **Bestilt** for én eller flere varer som er tilknyttet til dette reservasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="64a6b-145">Hvis eksisterende reservasjonshierarki for en vare ikke tillater partispesifikasjon på ordren, kan du tilordne den på nytt til et reservasjonshierarki som tillater partispesifikasjon, forutsatt at hierarkinivåstrukturen er lik i begge hierarkier.</span><span class="sxs-lookup"><span data-stu-id="64a6b-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="64a6b-146">Bruk **Endre reservasjonshierarki for varer**-funksjonen til å gjennomføre omtilordningen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="64a6b-147">Denne endringen kan være relevant når du vil forhindre fleksibel partireservering for et delsett av partisporede elementer, men tillate den for resten av produktporteføljen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="64a6b-148">Uavhengig av om du har merket av i **Tillat reservasjon på etterspørselsordre**-avmerkingsboksen, gjelder følgende: Hvis du ikke vil reservere et spesifikt partinummer for varen på en ordrelinje, vil standard lagerstyringslogikk som er gyldig for et "Parti under\[plassering\]"-reservasjonshierarki, fremdeles gjelde.</span><span class="sxs-lookup"><span data-stu-id="64a6b-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="64a6b-149">Reservere et bestemt partinummer for en kundeordre</span><span class="sxs-lookup"><span data-stu-id="64a6b-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="64a6b-150">Etter at "Parti under\[plassering\]"-beholdningsreservasjonshierarki for en partisporet vare er satt opp for å tillate reservasjon av spesifikke partinumre på salgsordrer, kan salgsordreprosessorer ta imot kundeordrer for samme vare på en av følgende måter, avhengig av kundens forespørsel:</span><span class="sxs-lookup"><span data-stu-id="64a6b-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="64a6b-151">**Angi ordredetaljer uten å angi et partinummer** – Denne fremgangsmåten skal brukes når produktets partispesifikasjon ikke er viktig for kunden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="64a6b-152">Alle eksisterende prosesser som er knyttet til håndtering av en ordre av denne typen i systemet, forblir uendret.</span><span class="sxs-lookup"><span data-stu-id="64a6b-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="64a6b-153">Ingen ekstra hensyn kreves fra brukerne.</span><span class="sxs-lookup"><span data-stu-id="64a6b-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="64a6b-154">**Angi ordredetaljer og reserver et bestemt partinummer** – Denne fremgangsmåten skal brukes når kunden ber om et bestemt parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="64a6b-155">Vanligvis vil kunder be om et bestemt parti når de ombestiller et produkt som de har kjøpt tidligere.</span><span class="sxs-lookup"><span data-stu-id="64a6b-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="64a6b-156">Denne typen partispesifikk reservasjon omtales som *Ordreigangsatt reservasjon*.</span><span class="sxs-lookup"><span data-stu-id="64a6b-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="64a6b-157">Følgende sett med regler er gyldig når kvantiteter behandles, og et partinummer er bundet til en bestemt ordre:</span><span class="sxs-lookup"><span data-stu-id="64a6b-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="64a6b-158">For å tillate reservasjon av et spesifikt partinummer for en vare under "Parti under\[plassering\]"-reservasjonsretningslinjen må systemet reservere alle dimensjoner opp gjennom plasseringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="64a6b-159">Dette området inkluderer vanligvis nummerskiltdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="64a6b-160">Plasseringsdirektiver brukes ikke når det opprettes plukkarbeid for en salgslinje som bruker ordrebundet partireservering.</span><span class="sxs-lookup"><span data-stu-id="64a6b-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="64a6b-161">Under lagerbehandling av arbeid for ordrebundne partier har verken brukeren eller systemet lov til å endre partinummeret.</span><span class="sxs-lookup"><span data-stu-id="64a6b-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="64a6b-162">(Denne behandlingen omfatter unntakshåndtering.)</span><span class="sxs-lookup"><span data-stu-id="64a6b-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="64a6b-163">Det følgende eksempelet viser ende-til-ende-flyten.</span><span class="sxs-lookup"><span data-stu-id="64a6b-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="64a6b-164">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="64a6b-164">Example scenario</span></span>

<span data-ttu-id="64a6b-165">For dette eksempelet må demonstrasjonsdata være installert, og du må bruke **USMF**-demonstrasjonsdataselskapet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="64a6b-166">Sette opp et beholdningsreservasjonshierarki for å tillate partispesifikk reservasjon</span><span class="sxs-lookup"><span data-stu-id="64a6b-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="64a6b-167">Gå til **Lagerstyring** \> **Oppsett** \> **Beholdning \> Reservasjonshierarki**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="64a6b-168">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-168">Select **New**.</span></span>
3. <span data-ttu-id="64a6b-169">I **Navn**-feltet skriver du inn et navn (for eksempel **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="64a6b-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="64a6b-170">I **Beskrivelse**-feltet skriver du inn en beskrivelse (for eksempel **Parti under fleksibelt**).</span><span class="sxs-lookup"><span data-stu-id="64a6b-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="64a6b-171">I **Valgt**-feltet velger du **Serienummer** og **Eier**, og velg deretter venstre pilknapp for å flytte dem til **Tilgjengelig**-feltet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="64a6b-172">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-172">Select **OK**.</span></span>
7. <span data-ttu-id="64a6b-173">I raden for **Partinummer**-dimensjonsnivået merker du av i **Tillat reservasjon på etterspørselsordre**-avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="64a6b-174">**Nummerskilt**- og **Plassering**-nivåene velges automatisk, og du kan ikke fjerne avmerkingen i avmerkingsboksene for dem.</span><span class="sxs-lookup"><span data-stu-id="64a6b-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="64a6b-175">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="64a6b-176">Opprette et nytt frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="64a6b-176">Create a new released product</span></span>

1. <span data-ttu-id="64a6b-177">Angi de tre hoveddataparameterne for produktet ved å bruke disse verdiene:</span><span class="sxs-lookup"><span data-stu-id="64a6b-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="64a6b-178">I **Lagringsdimensjonsgruppe**-feltet velger du **Lager**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="64a6b-179">I **Sporingsdimensjonsgruppe**-feltet velger du **Parti-fys**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="64a6b-180">I **Reservasjonshierarki**-feltet velger du **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="64a6b-181">Opprett to partinumre, for eksempel **B11** og **B22**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="64a6b-182">Legg til varekvantiteter i beholdningen på lager ved hjelp av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="64a6b-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="64a6b-183">Lager</span><span class="sxs-lookup"><span data-stu-id="64a6b-183">Warehouse</span></span> | <span data-ttu-id="64a6b-184">Partinummer</span><span class="sxs-lookup"><span data-stu-id="64a6b-184">Batch number</span></span> | <span data-ttu-id="64a6b-185">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="64a6b-185">Location</span></span> | <span data-ttu-id="64a6b-186">Nummerskilt</span><span class="sxs-lookup"><span data-stu-id="64a6b-186">License plate</span></span> | <span data-ttu-id="64a6b-187">Antall</span><span class="sxs-lookup"><span data-stu-id="64a6b-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="64a6b-188">24</span><span class="sxs-lookup"><span data-stu-id="64a6b-188">24</span></span>        | <span data-ttu-id="64a6b-189">B11</span><span class="sxs-lookup"><span data-stu-id="64a6b-189">B11</span></span>          | <span data-ttu-id="64a6b-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="64a6b-190">BULK-001</span></span> | <span data-ttu-id="64a6b-191">Ingen</span><span class="sxs-lookup"><span data-stu-id="64a6b-191">None</span></span>          | <span data-ttu-id="64a6b-192">10</span><span class="sxs-lookup"><span data-stu-id="64a6b-192">10</span></span>       |
    | <span data-ttu-id="64a6b-193">24</span><span class="sxs-lookup"><span data-stu-id="64a6b-193">24</span></span>        | <span data-ttu-id="64a6b-194">B11</span><span class="sxs-lookup"><span data-stu-id="64a6b-194">B11</span></span>          | <span data-ttu-id="64a6b-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="64a6b-195">FL-001</span></span>   | <span data-ttu-id="64a6b-196">LP11</span><span class="sxs-lookup"><span data-stu-id="64a6b-196">LP11</span></span>          | <span data-ttu-id="64a6b-197">10</span><span class="sxs-lookup"><span data-stu-id="64a6b-197">10</span></span>       |
    | <span data-ttu-id="64a6b-198">24</span><span class="sxs-lookup"><span data-stu-id="64a6b-198">24</span></span>        | <span data-ttu-id="64a6b-199">B22</span><span class="sxs-lookup"><span data-stu-id="64a6b-199">B22</span></span>          | <span data-ttu-id="64a6b-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="64a6b-200">FL-002</span></span>   | <span data-ttu-id="64a6b-201">LP22</span><span class="sxs-lookup"><span data-stu-id="64a6b-201">LP22</span></span>          | <span data-ttu-id="64a6b-202">10</span><span class="sxs-lookup"><span data-stu-id="64a6b-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="64a6b-203">Angi salgsordredetaljer</span><span class="sxs-lookup"><span data-stu-id="64a6b-203">Enter sales order details</span></span>

1. <span data-ttu-id="64a6b-204">Gå til **Salg og markedsføring** \> **Salgsordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="64a6b-205">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-205">Select **New**.</span></span>
3. <span data-ttu-id="64a6b-206">På salgsordretoppteksten, i **Kundekonto**-feltet angir du **US-003**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="64a6b-207">Legg til en linje for den nye varen, og angi **10** som kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="64a6b-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="64a6b-208">Sørg for at **Lager**-feltet er satt til **24**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="64a6b-209">På **Salgsordrelinjer**-hurtigfanen velger du **Beholdning**, og går deretter til **Vedlikehold**-gruppen og velger **Partireservasjon**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="64a6b-210">**Partireservasjon**-siden viser en liste over partier som er tilgjengelige for reservasjon for ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="64a6b-211">For dette eksempelet viser den en kvantitet på **20** for partinummer **B11** og en kvantitet på **10** for partinummer **B22**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="64a6b-212">Vær oppmerksom på at **Partireservasjon**-siden ikke kan åpnes fra en linje hvis varen på denne linjen er assosiert med "Parti under\[plassering\]"-reservasjonshierarki med mindre den er satt opp for å tillate partispesifikk reservasjon.</span><span class="sxs-lookup"><span data-stu-id="64a6b-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="64a6b-213">Hvis du vil reservere et bestemt parti for en salgsordre, må du bruke **Partireservasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="64a6b-214">Hvis du oppgir partinummeret direkte på salgsordrelinjen, vil systemet fungere som om du skrev inn en spesifikk partiverdi for en vare som er underlagt "Parti under\[plassering\]"-reservasjonsretningslinjen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="64a6b-215">Når du lagrer linjen, får du en advarselmelding.</span><span class="sxs-lookup"><span data-stu-id="64a6b-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="64a6b-216">Hvis du bekrefter at partinummeret skal angis direkte på ordrelinjen, vil ikke linjen bli håndtert av den vanlige lagerbehandlingslogikken.</span><span class="sxs-lookup"><span data-stu-id="64a6b-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="64a6b-217">Hvis du reserverer kvantiteten fra **Reservasjon**-siden, vil ikke noe spesifikt parti bli reservert, og kjøringen av lageroperasjoner for linjen vil følge reglene som gjelder under "Parti under\[plassering\]"-reservasjonsretningslinjen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="64a6b-218">Generelt fungerer og samhandles denne siden med på samme måte som den fungerer og samhandles med for varer som har et tilknyttet reservasjonshierarki i "Parti over\[plassering\]"-typen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="64a6b-219">Følgende unntak gjelder imidlertid:</span><span class="sxs-lookup"><span data-stu-id="64a6b-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="64a6b-220">**Partinumre bundet til kildelinjen**-hurtigfanen viser partinumrene som er reservert for ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="64a6b-221">Partiverdiene i rutenettet vises gjennom oppfyllingssyklusen til ordrelinjen, inkludert lagerbehandlingsstadiene.</span><span class="sxs-lookup"><span data-stu-id="64a6b-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="64a6b-222">På **Oversikt**-hurtigfanen vises vanlig bestillingslinjereservasjon (det vil si reservasjon som utføres for dimensjonene over **Plassering**-nivået) derimot i rutenettet opp til tidspunktet lagerarbeidet opprettes på.</span><span class="sxs-lookup"><span data-stu-id="64a6b-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="64a6b-223">Deretter overtar arbeidsenheten linjereservasjonen, og linjereservasjonen vises ikke lenger på siden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="64a6b-224">**Partinumre bundet til kildelinjen**-hurtigfanen bidrar til å garantere at salgsordreprosessoren kan vise partinumrene som ble bundet til kundens ordre, når som helst i løpet av livssyklusen, opp gjennom faktureringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="64a6b-225">I tillegg til å reservere et bestemt parti kan en bruker manuelt velge den partispesifikke plasseringen og nummerskiltet i stedet for å la systemet velge dem automatisk.</span><span class="sxs-lookup"><span data-stu-id="64a6b-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="64a6b-226">Denne funksjonen er knyttet til utformingen av den ordreigangsatte partireservasjonsmekanismen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="64a6b-227">Som nevnt tidligere, gjelder følgende: Når et partinummer er reservert for en vare under "Parti under\[plassering\]"-reservasjonsretningslinjen må systemet reservere alle dimensjoner opp gjennom plasseringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="64a6b-228">Derfor vil lagerarbeid ha de samme lagringsdimensjonene som ble reservert av brukerne som jobbet med ordrene, og det kan hende at det ikke alltid representerer varelagerplasseringen som er praktisk, eller til og med mulig, for plukkeoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="64a6b-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="64a6b-229">Hvis ordreprosessorer er klare over lagerbegrensningene, kan det være lurt manuelt å velge de spesifikke plasseringene og nummerskiltene når de reserverer et parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="64a6b-230">I slike tilfeller må brukeren bruke **Visningsdimensjoner**-funksjonaliteten på sidetoppteksten og legge til plasseringen og nummerskiltet i rutenettet på **Oversikt**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="64a6b-231">På **Partireservasjon**-siden velger du linjen for parti **B11**, og velger deretter **Reserver linje**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="64a6b-232">Det er ikke angitt noen logikk for tilordning av plasseringen og nummerskilt under automatisk reservasjon.</span><span class="sxs-lookup"><span data-stu-id="64a6b-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="64a6b-233">Du kan angi kvantiteten manuelt i **Reservasjon**-feltet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="64a6b-234">Vær oppmerksom på at **Partinumre bundet til kildelinjen**-hurtigfanen, parti **B11** vises som **Bind**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Binde et spesifikt partinummer til en salgsordrelinje på Partireservasjon-siden](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="64a6b-236">Reservasjon av kvantiteten på en salgsordrelinje kan utføres på tvers av flere partier.</span><span class="sxs-lookup"><span data-stu-id="64a6b-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="64a6b-237">På samme måte kan reservasjon av samme parti utføres mot flere plasseringer og nummerskilt (hvis nummerskilt er aktivert for plasseringene).</span><span class="sxs-lookup"><span data-stu-id="64a6b-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="64a6b-238">Reservasjon av et bestemt parti for kvantiteten på en salgsordrelinje kan også være delvis.</span><span class="sxs-lookup"><span data-stu-id="64a6b-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="64a6b-239">Den totale kvantiteten på 100 enheter kan for eksempel reserveres slik at et spesifikt parti bindes til 20 enheter, mens 80 enheter reserveres på stedet og lagernivåer for ethvert tilgjengelig parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="64a6b-240">I dette tilfellet vil WMS håndtere plukkoperasjoner ved hjelp av to separate arbeidslinjer.</span><span class="sxs-lookup"><span data-stu-id="64a6b-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="64a6b-241">Gå til **Administrering av produktinformasjon** \> **Produkter** \> **Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="64a6b-242">Velg varen, og velg deretter **Administrer beholdning** \> **Vis** \> **Transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Ordreigangsatt reservasjon som lagertransaksjonstype](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="64a6b-244">Gjennomgå varens lagertransaksjoner som er knyttet til salgsordrelinjereservasjonen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="64a6b-245">En transaksjon der **Referanse**-feltet er satt til **Salgsordre** og **Utsted**-feltet er satt til **Reservert fysisk**, representerer ordrelinjereservasjonen for beholdningsdimensjonene over **Plassering**-nivået.</span><span class="sxs-lookup"><span data-stu-id="64a6b-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="64a6b-246">I henhold til varens beholdningsreservasjonshierarki er disse dimensjonene sted, lager og beholdningsstatus.</span><span class="sxs-lookup"><span data-stu-id="64a6b-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="64a6b-247">En transaksjon der **Referanse**-feltet er satt til **Ordreigangsatt reservasjon** og **Utsted**-feltet er satt til **Reservert fysisk**, representerer ordrelinjereservasjonen for det spesifikke partiet og alle beholdningsdimensjonene over det.</span><span class="sxs-lookup"><span data-stu-id="64a6b-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="64a6b-248">I henhold til varens beholdningsreservasjonshierarki er disse dimensjonene partinummer og plassering.</span><span class="sxs-lookup"><span data-stu-id="64a6b-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="64a6b-249">I dette eksempelet er plasseringen **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="64a6b-250">I salgsordretoppteksten velger du **Lager** \> **Handlinger** \> **Frigi til lager**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="64a6b-251">Ordrelinjen er nå bølgete, og det opprettes en belastning og et arbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="64a6b-252">Gjennomgå og behandle lagerarbeid som har ordreigangsatte partinumre</span><span class="sxs-lookup"><span data-stu-id="64a6b-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="64a6b-253">I **Salgsordrer**-hurtigfanen velger du **Lager** \> **Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="64a6b-254">Arbeidet som håndterer plukkoperasjonen for partikvantiteter som er bundet til salgsordrelinjen, har følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="64a6b-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="64a6b-255">For opprettelse av arbeid bruker systemet arbeidsmaler, men ikke plasseringsdirektiver.</span><span class="sxs-lookup"><span data-stu-id="64a6b-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="64a6b-256">Alle standardinnstillingene som er definert for arbeidsmaler, for eksempel et maksimalt antall plukklinjer eller en bestemt måleenhet, brukes for å bestemme når nytt arbeid skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="64a6b-257">Reglene som er assosiert med plasseringsdirektiver for identifisering av plukkplasseringer blir ikke vurdert, fordi den ordreigangsatte reservasjonen allerede angir alle beholdningsdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="64a6b-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="64a6b-258">Disse beholdningsdimensjonene inkluderer dimensjonene på lageroppbevaringsnivået.</span><span class="sxs-lookup"><span data-stu-id="64a6b-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="64a6b-259">Derfor arver arbeidet disse dimensjonene uten å måtte sjekke plasseringsdirektiver.</span><span class="sxs-lookup"><span data-stu-id="64a6b-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="64a6b-260">Partinummeret vises ikke på plukklinjen (noe som også er tilfelle for arbeidslinjen som opprettes for en vare som har et tilknyttet "Parti over\[plassering\]"-reservasjonshierarki). I stedet vises "fra"-partinummeret og alle andre lagringsdimensjoner på arbeidslinjens arbeidsbeholdningstransaksjon som det henvises til fra de tilhørende beholdningstransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="64a6b-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Lagerbeholdningstransaksjon for arbeid som stammer fra ordreigangsatt reservasjon](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="64a6b-262">Etter at arbeidet er opprettet, blir varens beholdningstransaksjon der **Referanse**-feltet er satt til **Ordreigangsatt reservasjon**, fjernet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="64a6b-263">Beholdningstransaksjonen der **Referanse**-feltet er satt til **Arbeid**, inneholder nå den fysiske reservasjonen for alle beholdningsdimensjoner for kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="64a6b-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="64a6b-264">Lageroperasjoner kan fortsette å håndtere utførelsen av arbeidet på vanlig måte.</span><span class="sxs-lookup"><span data-stu-id="64a6b-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="64a6b-265">Instruksjonene på mobilenheten vil imidlertid instruere arbeideren om å velge et bestemt partinummer.</span><span class="sxs-lookup"><span data-stu-id="64a6b-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="64a6b-266">I lagermiljøer der plasseringene er nummerskiltkontrollert, gjelder følgende: Etter at en arbeider har nådd en plassering som lagrer det samme partiet på flere nummerskilt, kan han eller hun velge fra et hvilket som helst nummerskilt som ikke allerede er reservert (for eksempel av en annen ordreigangsatt reservasjon eller arbeid som stammer fra en reservasjon av denne typen.)</span><span class="sxs-lookup"><span data-stu-id="64a6b-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="64a6b-267">Hvis det viser seg at det blir upraktisk å velge fra plasseringen som er spesifisert på arbeidslinjen, kan lageroperatørene bruke en av følgende handlinger for å omdirigere plukking av det spesifikke partiet fra en mer praktisk plassering:</span><span class="sxs-lookup"><span data-stu-id="64a6b-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="64a6b-268">Standardhandlingen **Overstyr plassering** på en mobilenhet (forutsatt at lagerarbeiderens **Tillat overstyring av plukkplassering**-innstilling er aktivert)</span><span class="sxs-lookup"><span data-stu-id="64a6b-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="64a6b-269">**Endre plassering**-handlingen på**Arbeidslistedetaljer**-siden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="64a6b-270">Fullfør plukking og plassering av arbeidet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="64a6b-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="64a6b-271">Antallet **10** for partinummer **B11** er nå valgt for salgsordrelinjen og plassert i **Båsdør**-plasseringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="64a6b-272">På dette tidspunktet er det klart til å lastes på lastebilen og sendes til kundens adresse.</span><span class="sxs-lookup"><span data-stu-id="64a6b-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="64a6b-273">Unntakshåndtering av lagerarbeid som har ordreigangsatte partinumre</span><span class="sxs-lookup"><span data-stu-id="64a6b-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="64a6b-274">Lagerarbeid for plukking av ordreigangsatte partinumre er underlagt samme standard lagerunntakshåndtering og -handlinger som vanlig arbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="64a6b-275">Generelt kan det åpne arbeidet eller arbeidslinjen avbrytes. De kan avbrytes fordi en brukerplassering er full, det kan mangle tilstrekkelig antall, og de kan oppdateres på grunn av en bevegelse.</span><span class="sxs-lookup"><span data-stu-id="64a6b-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="64a6b-276">Tilsvarende kan den valgte kvantiteten arbeid som allerede er fullført, reduseres, eller arbeidet kan reverseres.</span><span class="sxs-lookup"><span data-stu-id="64a6b-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="64a6b-277">Følgende nøkkelregel brukes for alle disse unntakshåndteringshandlingene: Partinummeret som var reservert for kunden, kan aldri erstattes med et annet partinummer, men lagringsdimensjonene (plassering og nummerskilt) kan endres gjennom enten en manuell oppdatering utført av brukeren eller en automatisk oppdatering utført av systemet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="64a6b-278">Den automatiske oppdateringen er basert på den samme tilfeldige tilordningen av lagringsdimensjoner som gjaldt da et spesifikt parti ble reservert automatisk, men ingen lagringsdimensjoner ble spesifisert.</span><span class="sxs-lookup"><span data-stu-id="64a6b-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="64a6b-279">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="64a6b-279">Example scenario</span></span>

<span data-ttu-id="64a6b-280">Et eksempel på dette scenarioet er en situasjon der tidligere avsluttet arbeid plukkes fra hverandre ved å benytte **Reduser plukket kvantitet**-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="64a6b-281">Dette eksemplet er en fortsettelse av det forrige eksempelet i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="64a6b-282">Gå til **Lagerstyring** \> **Belastninger** \> **Aktive belastninger**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="64a6b-283">Velg belastningen som ble opprettet i forbindelse med forsendelsen av salgsordren.</span><span class="sxs-lookup"><span data-stu-id="64a6b-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="64a6b-284">Gå til **Last inn ordrelinjer**-hurtigfanen og velg **Reduser plukket kvantitet**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="64a6b-285">Gå til **Reduser plukket kvantitet**-siden i **Flytt til plassering**-feltet og velg **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="64a6b-286">I **Flytt til nummerskilt**-feltet velger du **LP33**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="64a6b-287">I rutenettet, i **Beholdningskvantitet som skal plukkes vekk**-feltet, angir du **10**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="64a6b-288">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-288">Select **OK**.</span></span>

<span data-ttu-id="64a6b-289">Her er resultatene av handlingen med vekkplukking:</span><span class="sxs-lookup"><span data-stu-id="64a6b-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="64a6b-290">Statusen til det tidligere lukkede verket er satt til **Avbrutt**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="64a6b-291">Nytt arbeid av **Beholdningsbevegelse**-typen opprettes for det vekkplukkede antallet **10** for partinummer **B11**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="64a6b-292">Dette arbeidet representerer bevegelsen fra **Båsdør**-plasseringen til nummerskiltet **LP33** på plasseringen **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="64a6b-293">Status er satt til **Lukket**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="64a6b-294">Systemet reserverer partinummeret som opprinnelig ble bestilt, på nytt og tilordner plasseringen og nummerskilt-ID-er.</span><span class="sxs-lookup"><span data-stu-id="64a6b-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="64a6b-295">(Denne prosessen tilsvarer kjøring av **Reserver linje**-funksjonen for ordrelinjen for et gitt partinummer).</span><span class="sxs-lookup"><span data-stu-id="64a6b-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="64a6b-296">Som et resultat vises parti **B11** som bundet på **Partinumre bundet til kildelinje**-hurtigfanen på **Partireservasjon**-siden, og **Reservasjon**-feltet inneholder antallet **10** for partinummer **B11**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="64a6b-297">I tillegg er **Plassering**-feltet satt til **FL-001**, og **Nummerskilt**-feltet er satt til **LP11**.</span><span class="sxs-lookup"><span data-stu-id="64a6b-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="64a6b-298">(Du kan legge til disse feltene i rutenettet hvis de ikke er synlige.)</span><span class="sxs-lookup"><span data-stu-id="64a6b-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="64a6b-299">Følgende tabeller inneholder en oversikt som viser hvordan systemet håndterer ordreigangsatt partireservasjon for bestemte lagerhandlinger.</span><span class="sxs-lookup"><span data-stu-id="64a6b-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="64a6b-300">Hvis du vil tolke innholdet i tabellene, må du anta at hver lagerhandling kjøres i konteksten av eksisterende lagerarbeid som stammer fra en ordreigangsatt partireservasjon, eller at utførelsen av hver lagerhandling påvirker arbeid av denne typen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="64a6b-301">I disse tabellene angir "Partikvantitet er tilgjengelig"-kolonnen om en partikvantitet er tilgjengelig, i tillegg til kvantiteten som allerede er reservert for gjeldende ordreigangsatte reservasjoner, eller som allerede er reservert av lagerarbeidet som stammer fra reservasjoner av denne typen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="64a6b-302">Overstyr plukkplasseringen for det åpne arbeidet</span><span class="sxs-lookup"><span data-stu-id="64a6b-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64a6b-303">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="64a6b-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="64a6b-304">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="64a6b-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="64a6b-305">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="64a6b-305">Key user steps</span></span></th>
<th><span data-ttu-id="64a6b-306">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="64a6b-306">Warehouse work</span></span></th>
<th><span data-ttu-id="64a6b-307">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="64a6b-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="64a6b-308"><strong>Tillat overstyring av plukkplassering</strong>-alternativet er aktivert for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="64a6b-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="64a6b-309">Ja</span><span class="sxs-lookup"><span data-stu-id="64a6b-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-310">Velg <strong>Overstyr plassering</strong>-menyelementet på Warehouse Mobile App (WMA) når du begynner plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-310">Select the <strong>Override location</strong> menu item on the Warehouse Mmobile App (WMA) when you start picking work.</span></span></li>
<li><span data-ttu-id="64a6b-311">Velg <strong>Foreslå</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="64a6b-312">Bekreft den nye plasseringen som foreslås, basert på tilgjengeligheten av partikvantitet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="64a6b-313">For gjeldende arbeid oppstår det følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="64a6b-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="64a6b-314">Plasseringen på plukklinjen oppdateres til den nye plasseringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="64a6b-315">(Hvis plasseringen er navneskiltstyrt, tilordnes et tilfeldig nummerskilt til arbeidslagertransaksjonen, og arbeideren kan plukke et hvilket som helst nummerskilt som har tilgjengelig kvantitet.)</span><span class="sxs-lookup"><span data-stu-id="64a6b-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="64a6b-316">Hvis kvantiteten blir funnet for mer enn ett nummerskilt på den nye plasseringen, blir den opprinnelige plukklinjen delt opp i flere linjer for å matche hvert nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="64a6b-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="64a6b-317">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-318">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-319">Velg <strong>Overstyr plassering</strong>-menyelementet på WMA når du starter plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-319">Select the <strong>Override location</strong> menu item on the WMA when you start picking work.</span></span></li>
<li><span data-ttu-id="64a6b-320">Angi en plassering manuelt.</span><span class="sxs-lookup"><span data-stu-id="64a6b-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="64a6b-321"><strong>Overstyr plassering</strong>-handlingen er ikke mulig.</span><span class="sxs-lookup"><span data-stu-id="64a6b-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="64a6b-322">Den mislykkes, og det oppstår en feil.</span><span class="sxs-lookup"><span data-stu-id="64a6b-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="64a6b-323">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="64a6b-324">Full knapp – del opp en arbeidslinje på grunn av overflyt på brukerplasseringen</span><span class="sxs-lookup"><span data-stu-id="64a6b-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64a6b-325">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="64a6b-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="64a6b-326">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="64a6b-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="64a6b-327">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="64a6b-327">Key user steps</span></span></th>
<th><span data-ttu-id="64a6b-328">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="64a6b-328">Warehouse work</span></span></th>
<th><span data-ttu-id="64a6b-329">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="64a6b-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64a6b-330"><strong>Tillat oppdeling av arbeid</strong>-alternativet er aktivert på mobilenhetens menyelement.</span><span class="sxs-lookup"><span data-stu-id="64a6b-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="64a6b-331">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-332">Velg <strong>Full</strong>-menyelementet på WMA når du behandler plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-332">Select the <strong>Full</strong> menu item on the WMA when you process picking work.</span></span></li>
<li><span data-ttu-id="64a6b-333">I <strong>Plukkvantitet</strong>-feltet angir du en delvis kvantitet for den påkrevde plukkingen for å indikere hele kapasiteten.</span><span class="sxs-lookup"><span data-stu-id="64a6b-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="64a6b-334">I gjeldende arbeid oppdateres kvantiteten til den gjenværende kvantiteten som må plukkes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="64a6b-335">Nytt arbeid for den plukkede kvantiteten opprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="64a6b-336">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="64a6b-337">Redusere den plukkede kvantiteten for fullført arbeid (fra en belastning)</span><span class="sxs-lookup"><span data-stu-id="64a6b-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64a6b-338">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="64a6b-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="64a6b-339">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="64a6b-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="64a6b-340">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="64a6b-340">Key user steps</span></span></th>
<th><span data-ttu-id="64a6b-341">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="64a6b-341">Warehouse work</span></span></th>
<th><span data-ttu-id="64a6b-342">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="64a6b-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="64a6b-343">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-343">Not applicable</span></span></td>
<td><span data-ttu-id="64a6b-344">Ja</span><span class="sxs-lookup"><span data-stu-id="64a6b-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-345">Åpne <strong>Reduser plukket kvantitet</strong>-siden fra belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="64a6b-346">Angi den fullstendige kvantiteten som skal plukkes vekk.</span><span class="sxs-lookup"><span data-stu-id="64a6b-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="64a6b-347">Velg "Flytt til"-plassering/-nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="64a6b-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="64a6b-348">Arbeid som er knyttet til belastningslinjen, avbrytes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="64a6b-349">Nytt arbeid for beholdningsbevegelsen opprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="64a6b-350">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="64a6b-351">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="64a6b-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-352">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-352">No</span></span></td>
<td><span data-ttu-id="64a6b-353">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-353">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-354">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-354">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-355">Kvantiteten reserveres på nytt for samme parti, samt for samme plassering og nummerskilt (hvis plasseringen er nummerskiltstyrt) som ble angitt under vekkplukking.</span><span class="sxs-lookup"><span data-stu-id="64a6b-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="64a6b-356">Flytte en vare i et lager</span><span class="sxs-lookup"><span data-stu-id="64a6b-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="64a6b-357">Denne lagerhandlingen gjelder bare for bevegelse av **Arbeidsopprettelsesprosess**-typen, ikke for bevegelse etter mal.</span><span class="sxs-lookup"><span data-stu-id="64a6b-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64a6b-358">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="64a6b-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="64a6b-359">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="64a6b-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="64a6b-360">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="64a6b-360">Key user steps</span></span></th>
<th><span data-ttu-id="64a6b-361">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="64a6b-361">Warehouse work</span></span></th>
<th><span data-ttu-id="64a6b-362">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="64a6b-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="64a6b-363"><strong>Tillat bevegelse av beholdning med tilhørende arbeid</strong>-alternativet er aktivert for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="64a6b-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="64a6b-364">Ja</span><span class="sxs-lookup"><span data-stu-id="64a6b-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-365">Start en flytting på WMA.</span><span class="sxs-lookup"><span data-stu-id="64a6b-365">Start a movement on the WMA.</span></span></li>
<li><span data-ttu-id="64a6b-366">Angi "fra"- og "til"-plasseringene.</span><span class="sxs-lookup"><span data-stu-id="64a6b-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="64a6b-367">For alt eksisterende arbeid som påvirkes av flyttingen, oppdateres plukkplasseringen til den nye plasseringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="64a6b-368">Nytt arbeid for beholdningsbevegelsen opprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="64a6b-369">Alle eksisterende reservasjoner som påvirkes av kvantitetsbevegelsen fra den gitte plasseringen, reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="64a6b-370">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="64a6b-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-371">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-371">No</span></span></td>
<td><span data-ttu-id="64a6b-372">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-372">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-373">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-373">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-374">Alle eksisterende reservasjoner som påvirkes av kvantitetsbevegelsen fra den gitte plasseringen, reserveres for samme parti, samt for den nye "til"- plasseringen og det nye "til"-nummerskiltet (hvis plasseringen er nummerskiltstyrt).</span><span class="sxs-lookup"><span data-stu-id="64a6b-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="64a6b-375">Reversere den plukkede kvantiteten for fullført arbeid (fra en belastning eller en bølge)</span><span class="sxs-lookup"><span data-stu-id="64a6b-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64a6b-376">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="64a6b-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="64a6b-377">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="64a6b-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="64a6b-378">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="64a6b-378">Key user steps</span></span></th>
<th><span data-ttu-id="64a6b-379">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="64a6b-379">Warehouse work</span></span></th>
<th><span data-ttu-id="64a6b-380">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="64a6b-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="64a6b-381">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-381">Not applicable</span></span></td>
<td><span data-ttu-id="64a6b-382">Ja</span><span class="sxs-lookup"><span data-stu-id="64a6b-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-383">Åpne <strong>Reverser arbeid</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="64a6b-384">På forespørselssiden velger du <strong>Etterlat varer på gjeldende plassering</strong>-alternativet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="64a6b-385">Alt arbeid som er knyttet til belastningen, avbrytes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="64a6b-386">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="64a6b-387">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="64a6b-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-388">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-388">No</span></span></td>
<td><span data-ttu-id="64a6b-389">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-389">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-390">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-390">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-391">Kvantiteten reserveres på nytt for samme parti, samt for plasseringen og nummerskiltet der kvantiteten ble etterlatt ved reversering.</span><span class="sxs-lookup"><span data-stu-id="64a6b-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-392">Ja</span><span class="sxs-lookup"><span data-stu-id="64a6b-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-393">Åpne <strong>Reverser arbeid</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="64a6b-394">På forespørselssiden velger du <strong>Tilordne varer til denne plasseringen</strong>-alternativet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="64a6b-395">Det gjeldende arbeidet avbrytes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="64a6b-396">Nytt arbeid for beholdningsbevegelsen opprettes og lukkes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="64a6b-397">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="64a6b-398">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="64a6b-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-399">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-399">No</span></span></td>
<td><span data-ttu-id="64a6b-400">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-400">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-401">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-401">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-402">Kvantiteten reserveres på nytt for samme parti, samt for plasseringen og nummerskiltet som kvantiteten ble tilordnet til ved reversering.</span><span class="sxs-lookup"><span data-stu-id="64a6b-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-403">Ja/nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-404">Åpne <strong>Reverser arbeid</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="64a6b-405">På forespørselssiden velger du <strong>Flytt varer til denne plasseringen</strong>-alternativet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="64a6b-406">Reversering støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="64a6b-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="64a6b-407">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-408">Ja/nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-409">Åpne <strong>Reverser arbeid</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="64a6b-410">På forespørselssiden velger du <strong>Flytt varer basert på plasseringsdirektiver</strong>-alternativet.</span><span class="sxs-lookup"><span data-stu-id="64a6b-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="64a6b-411">Reversering støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="64a6b-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="64a6b-412">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="64a6b-413">Plukk en kvantitet med mangler – Registrer kvantiteten som fysisk ikke funnet på plasseringen/nummerskiltet mens du utfører plukkarbeidet</span><span class="sxs-lookup"><span data-stu-id="64a6b-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64a6b-414">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="64a6b-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="64a6b-415">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="64a6b-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="64a6b-416">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="64a6b-416">Key user steps</span></span></th>
<th><span data-ttu-id="64a6b-417">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="64a6b-417">Warehouse work</span></span></th>
<th><span data-ttu-id="64a6b-418">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="64a6b-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="64a6b-419">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Ingen</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="64a6b-420">Ja</span><span class="sxs-lookup"><span data-stu-id="64a6b-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-421">Velg <strong>Plukk med mangler</strong>-menyelementet på WMA når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-421">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="64a6b-422">I feltet <strong>Plukkekvantitet</strong> angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="64a6b-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="64a6b-423">I <strong>Årsak</strong>-feltet angir du <strong>Ingen ny fordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="64a6b-424">Gjeldende arbeid lukkes, og den plukkede kvantiteten er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="64a6b-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="64a6b-425">Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="64a6b-426">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="64a6b-427">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="64a6b-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-428">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-428">No</span></span></td>
<td><span data-ttu-id="64a6b-429">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="64a6b-430">Handlingen for plukking med mangler mislykkes, og det oppstår en feil.</span><span class="sxs-lookup"><span data-stu-id="64a6b-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="64a6b-431">Gjeldende arbeid forblir åpent.</span><span class="sxs-lookup"><span data-stu-id="64a6b-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="64a6b-432">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="64a6b-433">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Ingen</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="64a6b-434">Ja</span><span class="sxs-lookup"><span data-stu-id="64a6b-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-435">Velg <strong>Plukk med mangler</strong>-menyelementet på WMA når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-435">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="64a6b-436">I feltet <strong>Plukkekvantitet</strong> angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="64a6b-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="64a6b-437">I <strong>Årsak</strong>-feltet angir du <strong>Ingen ny fordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="64a6b-438">Gjeldende arbeid lukkes, og den plukkede kvantiteten er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="64a6b-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="64a6b-439">Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="64a6b-440">Alle eksisterende reservasjoner som påvirkes av kvantitetsjusteringen i plasseringen for plukking med mangler, reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="64a6b-441">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="64a6b-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-442">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-442">No</span></span></td>
<td><span data-ttu-id="64a6b-443">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-443">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-444">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-444">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-445">Alle eksisterende reservasjoner som påvirkes av kvantitetsjusteringen i plasseringen for plukking med mangler, fjernes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-446">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Manuell</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Nei/Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="64a6b-447">I tillegg er <strong>Tillat manuell omfordeling av varer</strong>-alternativet aktivert for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="64a6b-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="64a6b-448">Ja</span><span class="sxs-lookup"><span data-stu-id="64a6b-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-449">Velg <strong>Plukk med mangler</strong>-menyelementet på WMA når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-449">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="64a6b-450">I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="64a6b-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="64a6b-451">I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med manuell omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="64a6b-452">Velg plasseringen/nummerskiltet i listen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="64a6b-453">For gjeldende arbeid oppstår det følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="64a6b-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="64a6b-454">Plukklinjen lukkes, og den plukkede kvantiteten er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="64a6b-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="64a6b-455">Plasseringslinjen avbrytes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="64a6b-456">Det opprettes en ny plukklinje.</span><span class="sxs-lookup"><span data-stu-id="64a6b-456">A new pick line is created.</span></span> <span data-ttu-id="64a6b-457">Den bruker plasseringen/nummerskiltet som brukeren valgte.</span><span class="sxs-lookup"><span data-stu-id="64a6b-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="64a6b-458">Det opprettes en ny plasseringslinje.</span><span class="sxs-lookup"><span data-stu-id="64a6b-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="64a6b-459">Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="64a6b-460">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-461">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Manuell</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="64a6b-462">I tillegg er <strong>Tillat manuell omfordeling av varer</strong>-alternativet aktivert for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="64a6b-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="64a6b-463">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-464">Velg <strong>Plukk med mangler</strong>-menyelementet på WMA når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-464">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="64a6b-465">I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="64a6b-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="64a6b-466">I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med manuell omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="64a6b-467">Handlingen for plukking med mangler mislykkes, og det oppstår en feil.</span><span class="sxs-lookup"><span data-stu-id="64a6b-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="64a6b-468">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-469">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Manuell</strong>, <strong>Juster beholdning</strong> = <strong>Ja</strong> og <strong>Fjern reservasjoner</strong> = <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="64a6b-470">I tillegg er <strong>Tillat manuell omfordeling av varer</strong>-alternativet aktivert for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="64a6b-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="64a6b-471">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-472">Velg <strong>Plukk med mangler</strong>-menyelementet på WMA når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-472">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="64a6b-473">I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="64a6b-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="64a6b-474">I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med manuell omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="64a6b-475">Velg plasseringen/nummerskiltet i listen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="64a6b-476">For gjeldende arbeid oppstår det følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="64a6b-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="64a6b-477">Plukklinjen lukkes, og den plukkede kvantiteten er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="64a6b-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="64a6b-478">Plasseringslinjen avbrytes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="64a6b-479">Det opprettes en beholdningstransaksjon av <strong>Opptelling</strong>-typen, og <strong>Solgt</strong>-utstedelsestypen opprettes for å representere justeringen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="64a6b-480">Alle eksisterende reservasjoner som påvirkes av kvantitetsjusteringen i plasseringen/nummerskiltet for plukking med mangler, fjernes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-481">Et arbeidsunntak av <strong>Plukk med mangler</strong>-typen settes opp, der <strong>Ny fordeling av vare</strong> = <strong>Automatisk</strong>, <strong>Juster beholdning</strong> = <strong>Ja/Nei</strong> og <strong>Fjern reservasjoner</strong> = <strong>Ja/Nei</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="64a6b-482">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="64a6b-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-483">Velg <strong>Plukk med mangler</strong>-menyelementet på WMA når du kjører plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-483">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="64a6b-484">I <strong>Kvantitet for plukking med mangler</strong>-feltet angir du <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="64a6b-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="64a6b-485">I <strong>Årsak</strong>-feltet velger du <strong>Plukking med mangler med automatisk omfordeling</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="64a6b-486">Plukking med mangler som involverer automatisk omfordeling, støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="64a6b-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="64a6b-487">Plukking med mangler som involverer automatisk omfordeling, støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="64a6b-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="64a6b-488">Endre beholdningsstatusen</span><span class="sxs-lookup"><span data-stu-id="64a6b-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="64a6b-489">Denne lagerhandlingen kan utføres fra flere inngangspunkter.</span><span class="sxs-lookup"><span data-stu-id="64a6b-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="64a6b-490">I eksempelet som vises her, benyttes **Beholdningsstatusendring**-handlingen på **På lager etter plassering**-siden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64a6b-491">Nøkkeloppsettsparameter</span><span class="sxs-lookup"><span data-stu-id="64a6b-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="64a6b-492">Partikvantitet er tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="64a6b-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="64a6b-493">Nøkkelbrukertrinn</span><span class="sxs-lookup"><span data-stu-id="64a6b-493">Key user steps</span></span></th>
<th><span data-ttu-id="64a6b-494">Lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="64a6b-494">Warehouse work</span></span></th>
<th><span data-ttu-id="64a6b-495">Ordreigangsatt partireservasjon</span><span class="sxs-lookup"><span data-stu-id="64a6b-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="64a6b-496">I <strong>Lager</strong>-fanen, i <strong>Lager</strong>-oppføringen, er <strong>Fjern reservasjoner og merkinger</strong>-feltet satt til <strong>Reservasjoner</strong> eller <strong>Merkinger og reservasjoner</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="64a6b-497">Ja</span><span class="sxs-lookup"><span data-stu-id="64a6b-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-498">Velg en spesifikk plassering.</span><span class="sxs-lookup"><span data-stu-id="64a6b-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="64a6b-499">Velg en linje som har et spesifikt element, en spesifikk plassering og et spesifikt nummerskilt (hvis plasseringen er nummerskiltstyrt).</span><span class="sxs-lookup"><span data-stu-id="64a6b-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="64a6b-500">Velg <strong>Beholdningsstatusendring</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="64a6b-501">Sett <strong>Beholdningsstatus</strong>-feltet til <strong>Blokkering</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="64a6b-502">Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="64a6b-503">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="64a6b-504">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="64a6b-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="64a6b-505">Det opprettes to beholdningstransaksjoner av <strong>Beholdningsstatusendring</strong>-typen for å representere endringen i beholdningsstatusdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="64a6b-506">En beholdningstransaksjon av <strong>Beholdningsblokkering</strong>-typen og <strong>Reservert fysisk</strong>-utstedelsestypen opprettes for å representere reservasjonen av den blokkerte kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="64a6b-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-507">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-507">No</span></span></td>
<td><span data-ttu-id="64a6b-508">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-508">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-509">Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="64a6b-510">Reservasjonen fjernes.</span><span class="sxs-lookup"><span data-stu-id="64a6b-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="64a6b-511">Det opprettes to beholdningstransaksjoner av <strong>Beholdningsstatusendring</strong>-typen for å representere endringen i beholdningsstatusdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="64a6b-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="64a6b-512">En beholdningstransaksjon av <strong>Beholdningsblokkering</strong>-typen og <strong>Reservert fysisk</strong>-utstedelsestypen opprettes for å representere reservasjonen av den blokkerte kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="64a6b-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="64a6b-513">I <strong>Lager</strong>-fanen, i <strong>Lager</strong>-oppføringen, er <strong>Fjern reservasjoner og merkinger</strong>-feltet satt til <strong>Ingen</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="64a6b-514">Ja</span><span class="sxs-lookup"><span data-stu-id="64a6b-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="64a6b-515">Velg en spesifikk plassering.</span><span class="sxs-lookup"><span data-stu-id="64a6b-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="64a6b-516">Velg en linje som har et spesifikt element, en spesifikk plassering og et spesifikt nummerskilt (hvis plasseringen er nummerskiltstyrt).</span><span class="sxs-lookup"><span data-stu-id="64a6b-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="64a6b-517">Velg <strong>Beholdningsstatusendring</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="64a6b-518">Sett <strong>Beholdningsstatus</strong>-feltet til <strong>Blokkering</strong>.</span><span class="sxs-lookup"><span data-stu-id="64a6b-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="64a6b-519">Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="64a6b-520">Kvantiteten reserveres på nytt for samme parti.</span><span class="sxs-lookup"><span data-stu-id="64a6b-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="64a6b-521">Systemet tilordner tilfeldig en plassering og et nummerskilt (hvis plasseringen er nummerskiltstyrt) der kvantiteten er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="64a6b-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64a6b-522">Nei</span><span class="sxs-lookup"><span data-stu-id="64a6b-522">No</span></span></td>
<td><span data-ttu-id="64a6b-523">Se den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="64a6b-523">See the previous row.</span></span></td>
<td><span data-ttu-id="64a6b-524">Beholdningsstatusendringer er ikke tillatt for kvantiteter som er reservert for arbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="64a6b-525">Beholdningsstatusendringer er ikke tillatt.</span><span class="sxs-lookup"><span data-stu-id="64a6b-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="64a6b-526">Begrensninger</span><span class="sxs-lookup"><span data-stu-id="64a6b-526">Limitations</span></span>

- <span data-ttu-id="64a6b-527">Den fleksible funksjonaliteten for dimensjonsreservasjon på lagernivå støtter ikke følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="64a6b-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="64a6b-528">Administrering av faktisk vekt</span><span class="sxs-lookup"><span data-stu-id="64a6b-528">Catch weight management</span></span>
    - <span data-ttu-id="64a6b-529">Fysisk negativt lager</span><span class="sxs-lookup"><span data-stu-id="64a6b-529">Physical negative inventory</span></span>
    - <span data-ttu-id="64a6b-530">Reservasjon mot bestilt forsyning</span><span class="sxs-lookup"><span data-stu-id="64a6b-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="64a6b-531">Plukking av overføringsordrer og råvarer</span><span class="sxs-lookup"><span data-stu-id="64a6b-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="64a6b-532">Regelen for konsolidering av containere for pakking etter direktivenhet har begrensninger.</span><span class="sxs-lookup"><span data-stu-id="64a6b-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="64a6b-533">For ordreigangsatte reservasjoner anbefaler vi at du ikke bruker maler for containerbygging i tilfeller der **Pakk etter direktivenhet**-feltet er aktivert.</span><span class="sxs-lookup"><span data-stu-id="64a6b-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="64a6b-534">I gjeldende utforming brukes ikke plasseringsdirektiver når det opprettes lagerarbeid.</span><span class="sxs-lookup"><span data-stu-id="64a6b-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="64a6b-535">Derfor brukes bare den laveste enheten i enhetssekvensgruppen (beholdningsenheten) under bølgetrinnet containerbruk.</span><span class="sxs-lookup"><span data-stu-id="64a6b-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
