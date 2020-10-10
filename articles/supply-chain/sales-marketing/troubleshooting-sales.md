---
title: Feilsøke salgsordrer
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med salgsordrer.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6e51723915892f465ce09d09ee9ed622bab9451e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889463"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="2144a-103">Feilsøke salgsordrer</span><span class="sxs-lookup"><span data-stu-id="2144a-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="2144a-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="2144a-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="2144a-105">Skatteinformasjonen oppdateres ikke hvis jeg endrer lokasjonen i et salgsordrehode.</span><span class="sxs-lookup"><span data-stu-id="2144a-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2144a-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="2144a-106">Issue description</span></span>

<span data-ttu-id="2144a-107">Hvis område-, lager- eller leveringsadressen endres enten på et salgsordrehode eller på linjenivå, oppdateres ikke skatteinformasjonen for saken automatisk for linjene.</span><span class="sxs-lookup"><span data-stu-id="2144a-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2144a-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="2144a-108">Issue resolution</span></span>

<span data-ttu-id="2144a-109">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="2144a-109">This behavior is by design.</span></span> <span data-ttu-id="2144a-110">Problemet oppstår fordi leveringsadressen, området og lageret ikke automatisk blir endret på linjenivået.</span><span class="sxs-lookup"><span data-stu-id="2144a-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="2144a-111">Du må oppdatere dem manuelt.</span><span class="sxs-lookup"><span data-stu-id="2144a-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="2144a-112">Hvis det finnes to forretningsavtaler for samme periode eller overlappende perioder, blir alltid den samme avtalelinjen valgt.</span><span class="sxs-lookup"><span data-stu-id="2144a-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2144a-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="2144a-113">Issue description</span></span>

<span data-ttu-id="2144a-114">Hvis to forretningsavtaler er definert for samme periode eller ved overlappende perioder, ser det ut til at samme forretningsavtale blir valgt hver gang du oppretter salgsordrelinjer som inneholder disse varene.</span><span class="sxs-lookup"><span data-stu-id="2144a-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2144a-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="2144a-115">Issue resolution</span></span>

<span data-ttu-id="2144a-116">Hvis det finnes mer enn én forretningsavtale for en gitt dato, velges alltid forretningsavtalen som har den laveste prisen.</span><span class="sxs-lookup"><span data-stu-id="2144a-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="2144a-117">Hvis du vil ha mer informasjon, laster du ned følgende tekniske informasjon: [Forretningsavtaler i Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="2144a-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="2144a-118">Kan jeg koble en bestilling til en salgsordre for å imøtekomme etterspørselen?</span><span class="sxs-lookup"><span data-stu-id="2144a-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="2144a-119">Du kan opprette en bestilling fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="2144a-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="2144a-120">Hvis du vil ha mer informasjon, se [Opprette en bestilling fra en salgsordre](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="2144a-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="2144a-121">Jeg kan ikke avbryte eller slette en returordre eller en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="2144a-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="2144a-122">Du kan bare kansellere salgsordrer og returordrer som har statusen *Opprettet*.</span><span class="sxs-lookup"><span data-stu-id="2144a-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="2144a-123">Hvis du vil ha mer informasjon, se [Annullere en returordre](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="2144a-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="2144a-124">Når jeg prøver å annullere en salgsordre, får jeg feilen "Reservasjoner kan ikke fjernes fordi det er opprettet arbeid som er avhengig av reservasjonen".</span><span class="sxs-lookup"><span data-stu-id="2144a-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="2144a-125">Hvis arbeid er knyttet til en salgsordre, kan du ikke annullere salgsordren før arbeidet er annullert og tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="2144a-125">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="2144a-126">Dette kravet gjelder selv om arbeidet som er knyttet til salgsordren, er lukket.</span><span class="sxs-lookup"><span data-stu-id="2144a-126">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="2144a-127">Følg fremgangsmåten nedenfor for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="2144a-127">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="2144a-128">Avbryt arbeidet, og sett lageret tilbake på ønsket sted.</span><span class="sxs-lookup"><span data-stu-id="2144a-128">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="2144a-129">Gå til den relevante belastningen for salgsordren, og velg enten **Reduser plukket kvantitet** på belastningslinjen eller **Reverser arbeid** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2144a-129">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="2144a-130">Arbeidet har nå statusen *Avbrutt*, og nytt lagerflyttingsarbeid opprettes automatisk og behandles for å legge lager tilbake i lokasjonen som ble beskrevet da tilbakeføringen ble avbrutt.</span><span class="sxs-lookup"><span data-stu-id="2144a-130">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="2144a-131">Slett belastningen.</span><span class="sxs-lookup"><span data-stu-id="2144a-131">Delete the load.</span></span> <span data-ttu-id="2144a-132">Forsendelsen slettes også.</span><span class="sxs-lookup"><span data-stu-id="2144a-132">The shipment is also deleted.</span></span>
3. <span data-ttu-id="2144a-133">Du skal nå kunne gå til salgsordren og avbryte den.</span><span class="sxs-lookup"><span data-stu-id="2144a-133">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="2144a-134">Jeg kan ikke avbryte en konsernintern bestilling som er koblet til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="2144a-134">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2144a-135">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="2144a-135">Issue description</span></span>

<span data-ttu-id="2144a-136">Hvis du prøver å annullere en konsernintern bestilling som er koblet til en salgsordre, kan du få feilmelding om at antallet ikke kan reduseres, fordi det gjenstående oppdateringsantallet skifter fortegn.</span><span class="sxs-lookup"><span data-stu-id="2144a-136">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2144a-137">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="2144a-137">Issue resolution</span></span>

<span data-ttu-id="2144a-138">Dette problemet ble løst i Microsoft Dynamics 365 Supply Chain Management versjon 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="2144a-138">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="2144a-139">I denne versjonen og senere versjoner kan du nå annullere en konsernintern bestilling som er koblet til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="2144a-139">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="2144a-140">Kan jeg gjenopprette en fakturert salgsordre som er slettet?</span><span class="sxs-lookup"><span data-stu-id="2144a-140">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="2144a-141">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="2144a-141">Issue description</span></span>

<span data-ttu-id="2144a-142">En fakturert salgsordre ble slettet ved en feiltakelse, og du vil gjenopprette den eller vise detaljene for den.</span><span class="sxs-lookup"><span data-stu-id="2144a-142">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2144a-143">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="2144a-143">Issue resolution</span></span>

<span data-ttu-id="2144a-144">Hvis den slettede salgsordren allerede er fakturert, kan du gå til **Kundekonto \> Transaksjoner \> Original dokument \> Visningsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="2144a-144">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="2144a-145">Finn fakturaen du er på jakt etter, og velg den for å vise detaljene for den.</span><span class="sxs-lookup"><span data-stu-id="2144a-145">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="2144a-146">Disse detaljene omfatter salgsordrereferansen.</span><span class="sxs-lookup"><span data-stu-id="2144a-146">These details include the sales order reference.</span></span> <span data-ttu-id="2144a-147">Du bør også få tilgang til salgsordredetaljene fra denne siden.</span><span class="sxs-lookup"><span data-stu-id="2144a-147">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="2144a-148">Tidsfristen for et salgsordrehode finnes ikke i dataenheten SalesOrderHeaderV2Entity.</span><span class="sxs-lookup"><span data-stu-id="2144a-148">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="2144a-149">Tidsfristfeltet finnes ikke på enheten *SalesOrderHeaderV2Entity*.</span><span class="sxs-lookup"><span data-stu-id="2144a-149">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="2144a-150">Jeg må slette frittstående salgsordreposter.</span><span class="sxs-lookup"><span data-stu-id="2144a-150">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="2144a-151">Hvis du vil rydde opp i frittstående salgsordreposter, kan du kjøre den periodiske jobben *Salgsordresletting* ved å gå til et av følgende steder:</span><span class="sxs-lookup"><span data-stu-id="2144a-151">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="2144a-152">Salg og markedsføring \> Periodiske oppgaver \> Opprydding \> Slett salgsordrer</span><span class="sxs-lookup"><span data-stu-id="2144a-152">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="2144a-153">Detaljhandel og handel \> IT for Detaljhandel og handel \> Opprydding \> Slett salgsordrer</span><span class="sxs-lookup"><span data-stu-id="2144a-153">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="2144a-154">Finnes det en måte å beregne provisjon på fakturaer som allerede er postert?</span><span class="sxs-lookup"><span data-stu-id="2144a-154">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="2144a-155">Supply Chain Management støtter for øyeblikket ikke beregningen av provisjoner for posterte fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2144a-155">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="2144a-156">En buntvare støttes ikke i en konsernintern prosess.</span><span class="sxs-lookup"><span data-stu-id="2144a-156">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="2144a-157">Buntvaren er ikke tilgjengelig for bestillingen fordi hvis du undersøker salgsordrelinjene for buntvaren, vil du se at antallet er *0* (null), og at statusen er *Avbrutt*.</span><span class="sxs-lookup"><span data-stu-id="2144a-157">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Cancelled*.</span></span> <span data-ttu-id="2144a-158">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="2144a-158">This behavior is by design.</span></span> <span data-ttu-id="2144a-159">Salgsordren kjøper bare komponentene til buntvaren.</span><span class="sxs-lookup"><span data-stu-id="2144a-159">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="2144a-160">Selve buntvaren kjøpes ikke.</span><span class="sxs-lookup"><span data-stu-id="2144a-160">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="2144a-161">Hvis du må kjøpe en bunt, bør du vurdere om du må merke den som buntelement, fordi denne funksjonaliteten er utformet for scenarier med inntektsføring.</span><span class="sxs-lookup"><span data-stu-id="2144a-161">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is actually designed for revenue recognition scenarios.</span></span> <span data-ttu-id="2144a-162">Hvis du vil ha mer informasjon om buntvarer, se [Bunter](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="2144a-162">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
