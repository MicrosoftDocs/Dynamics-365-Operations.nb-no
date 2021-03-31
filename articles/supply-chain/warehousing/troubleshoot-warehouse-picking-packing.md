---
title: Feilsøke plukking og pakking
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du plukker og pakker i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 01e33b63e09a035f5243bd57faf53b522737c987
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223248"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="c750f-103">Feilsøke plukking og pakking</span><span class="sxs-lookup"><span data-stu-id="c750f-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c750f-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du plukker og pakker i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c750f-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="c750f-105">Jeg får følgende feilmelding: Dimensjonslokasjonen kan ikke stå tom hvis dimensjonsserienummeret er angitt.</span><span class="sxs-lookup"><span data-stu-id="c750f-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c750f-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c750f-106">Issue description</span></span>

<span data-ttu-id="c750f-107">Du får denne feilmeldingen hvis du oppretter en overføringsordre for en serievare ved hjelp av et lager som er aktivert for avansert lagerstyring (WMS), og etter at arbeidet er fullført, prøver du å bekrefte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="c750f-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c750f-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c750f-108">Issue resolution</span></span>

<span data-ttu-id="c750f-109">Feltet **Standard mottakssted** er tomt for et transittlager i fra-lageret.</span><span class="sxs-lookup"><span data-stu-id="c750f-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="c750f-110">Du kan løse dette problemet ved å angi en standard mottakssted i transittlageret.</span><span class="sxs-lookup"><span data-stu-id="c750f-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="c750f-111">Kontroller at denne plasseringen er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="c750f-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="c750f-112">Jeg får følgende feilmelding: Ugyldig nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="c750f-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c750f-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c750f-113">Issue description</span></span>

<span data-ttu-id="c750f-114">Du får denne feilmeldingen i lagerappen når du skanner en nummerskilt-ID.</span><span class="sxs-lookup"><span data-stu-id="c750f-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c750f-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c750f-115">Issue resolution</span></span>

<span data-ttu-id="c750f-116">Kontroller at det finnes en nummerskilt-ID i nummerskilttabellen, og at varene og antallene på nummerskiltet er tilgjengelige (med andre ord de er ikke blokkert).</span><span class="sxs-lookup"><span data-stu-id="c750f-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="c750f-117">Jeg får følgende feilmelding: Feltet Lastvekt (=-%1) kan bare inneholde positive tall.</span><span class="sxs-lookup"><span data-stu-id="c750f-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="c750f-118">Oppdateringen er avbrutt.</span><span class="sxs-lookup"><span data-stu-id="c750f-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c750f-119">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c750f-119">Issue description</span></span>

<span data-ttu-id="c750f-120">Du får denne feilmeldingen hvis det er åpent arbeid når du behandler arbeid fra emballasjelokasjoner til oppsamlingslokasjoner, eller fra oppsamlingslokasjoner til forankringslokasjoner.</span><span class="sxs-lookup"><span data-stu-id="c750f-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c750f-121">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c750f-121">Issue resolution</span></span>

<span data-ttu-id="c750f-122">Hvis du vil løse dette problemet, går du til **Systemadministrasjon \> Periodiske oppgaver \> Database \> Konsekvenskontroll** og kjører prosessen for **Konsekvenskontroll av lagerlastvekt**.</span><span class="sxs-lookup"><span data-stu-id="c750f-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="c750f-123">Jeg får følgende feilmelding: Antallet er ikke gyldig for enhet %1.</span><span class="sxs-lookup"><span data-stu-id="c750f-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c750f-124">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c750f-124">Issue description</span></span>

<span data-ttu-id="c750f-125">Du får denne feilmeldingen når du prøver å utføre en *delt plukking* på tvers av flere partier.</span><span class="sxs-lookup"><span data-stu-id="c750f-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c750f-126">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c750f-126">Issue resolution</span></span>

<span data-ttu-id="c750f-127">Lagerarbeideren må bruke *Plukking med mangler*-prosessen i lagerappen.</span><span class="sxs-lookup"><span data-stu-id="c750f-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="c750f-128">Hvis du prøver å plukke flere partier fra samme lokasjon, kan du også bruke **Fullstendig**-alternativet i lagerappen.</span><span class="sxs-lookup"><span data-stu-id="c750f-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="c750f-129">Jeg kan ikke flytte lager til en lokasjon som er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="c750f-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c750f-130">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c750f-130">Issue description</span></span>

<span data-ttu-id="c750f-131">Du kan ikke redusere plukket antall på en last.</span><span class="sxs-lookup"><span data-stu-id="c750f-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c750f-132">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c750f-132">Issue resolution</span></span>

<span data-ttu-id="c750f-133">I tidligere versjoner kan du ikke redusere plukket antall på en last.</span><span class="sxs-lookup"><span data-stu-id="c750f-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="c750f-134">Du kan imidlertid nå legge tilbake til en nummerskiltkontrollert lokasjon.</span><span class="sxs-lookup"><span data-stu-id="c750f-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="c750f-135">Du må angi både en **Lokasjon**-verdi og en **Nummerskilt**-verdi for lastlinjen på siden **Reduser plukket antall**.</span><span class="sxs-lookup"><span data-stu-id="c750f-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="c750f-136">Kan jeg skrive ut en følgeseddel eller pakkeinnhold etter lager?</span><span class="sxs-lookup"><span data-stu-id="c750f-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="c750f-137">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c750f-137">Issue description</span></span>

<span data-ttu-id="c750f-138">Du vil skrive ut en følgeseddel eller pakkeinnhold etter lager eller område på siden **Oppdatering av revisjonsmallinje**.</span><span class="sxs-lookup"><span data-stu-id="c750f-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c750f-139">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c750f-139">Issue resolution</span></span>

<span data-ttu-id="c750f-140">Når du skriver ut et dokument ved hjelp av innstillinger for utskriftsbehandling, begrenser du området (område/lager) til utskriftsbehandling i stedet for å velge **Rediger utskriftsinnstillinger** på siden **Oppgradering av revisjonsmallinje**.</span><span class="sxs-lookup"><span data-stu-id="c750f-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="c750f-141">Jeg kan ikke avbryte en følgeseddel etter at den er postert fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="c750f-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c750f-142">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c750f-142">Issue description</span></span>

<span data-ttu-id="c750f-143">Når plukk- og leveringsprosesser er aktivert for WMS, kan du ikke avbryte en følgeseddel etter at den er postert fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="c750f-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c750f-144">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c750f-144">Issue resolution</span></span>

<span data-ttu-id="c750f-145">Hvis du vil korrigere posterte følgesedler for varer som er aktivert for WMS, må du utføre posteringen fra lasten, ikke direkte fra ordren.</span><span class="sxs-lookup"><span data-stu-id="c750f-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="c750f-146">Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning.</span><span class="sxs-lookup"><span data-stu-id="c750f-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="c750f-147">Vanligvis kan en salgsordre som er plukket og sendt gjennom lagerstyringsprosesser, følgeseddeloppdateres fra lasten eller forsendelsen og selve salgsordredokumentet.</span><span class="sxs-lookup"><span data-stu-id="c750f-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="c750f-148">Hvis du imidlertid følgeseddeloppdaterer salgsordren fra salgsordredokumentet, kan fremdeles ikke følgeseddeltilbakeføring utføres fra lasten eller salgsordren.</span><span class="sxs-lookup"><span data-stu-id="c750f-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="c750f-149">Derfor anbefaler vi at du bruker følgeseddelposteringen fra lasten.</span><span class="sxs-lookup"><span data-stu-id="c750f-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="c750f-150">I dette tilfellet blir tilbakeføringen som må gjøres fra lasten, aktivert.</span><span class="sxs-lookup"><span data-stu-id="c750f-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="c750f-151">Jeg får følgende feilmelding: Finner ikke nok arbeid for gruppen.</span><span class="sxs-lookup"><span data-stu-id="c750f-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c750f-152">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c750f-152">Issue description</span></span>

<span data-ttu-id="c750f-153">Når du bruker prosessen *Systemkontrollert gruppeplukking*, hvis du konfigurerer en gruppeprofil der for eksempel 10 stillinger kan plukkes, fungerer prosessen som planlagt når det er nok arbeid til å plukke til 10 stillinger.</span><span class="sxs-lookup"><span data-stu-id="c750f-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="c750f-154">Men hvis det bare er åtte stillinger som skal plukkes, får du denne feilmeldingen fordi det ikke er nok arbeid for én gruppe.</span><span class="sxs-lookup"><span data-stu-id="c750f-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c750f-155">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c750f-155">Issue resolution</span></span>

<span data-ttu-id="c750f-156">Du kan løse dette problemet ved å redigere gruppeprofilen og sette **Aktiver stillinger**-alternativet til *Nei*.</span><span class="sxs-lookup"><span data-stu-id="c750f-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]