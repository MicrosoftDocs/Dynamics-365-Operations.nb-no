---
title: Feilsøke arbeidsflyter for innkjøp og leverandører
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med arbeidsflyter for innkjøp og leverandører.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
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
ms.openlocfilehash: 940a6c39ac83e7388d4e1a08b656b75df81ed801
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834402"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="2853b-103">Feilsøke arbeidsflyter for innkjøp og leverandører</span><span class="sxs-lookup"><span data-stu-id="2853b-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="2853b-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med arbeidsflyter for innkjøp og leverandører.</span><span class="sxs-lookup"><span data-stu-id="2853b-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="2853b-105">Feil under ny sending av en bestilling til arbeidsflyten etter en endring: "Endringer i bestilling X er bare tillatt i kladdetilstand når endringsadministrasjon er aktivert"</span><span class="sxs-lookup"><span data-stu-id="2853b-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="2853b-106">Dette problemet oppstår bare hvis bestillingen var i en *Bekreftet* tilstand før du forespurte endringer.</span><span class="sxs-lookup"><span data-stu-id="2853b-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="2853b-107">Hvis du ber om endringer mens bestillingen er i en *Godkjent* tilstand, kan arbeidsflyten behandles på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="2853b-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="2853b-108">Feilbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="2853b-108">Error description</span></span>

<span data-ttu-id="2853b-109">Følgende feil oppstår i arbeidsflyten når en bestilling sendes på nytt etter en endring:</span><span class="sxs-lookup"><span data-stu-id="2853b-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="2853b-110">Stoppet (feil): X++ Unntak: Endringer i bestilling PO0000569 er bare tillatt i tilstanden Utkast når endringsadministrasjon er aktivert på</span><span class="sxs-lookup"><span data-stu-id="2853b-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="2853b-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="2853b-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="2853b-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="2853b-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="2853b-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="2853b-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="2853b-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="2853b-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2853b-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="2853b-115">Issue resolution</span></span>

<span data-ttu-id="2853b-116">Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.</span><span class="sxs-lookup"><span data-stu-id="2853b-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="2853b-117">Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**.</span><span class="sxs-lookup"><span data-stu-id="2853b-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="2853b-118">Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="2853b-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="2853b-119">Problemet vil bli løst via [denne artikkelen i Microsoft Knowledge Base (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span><span class="sxs-lookup"><span data-stu-id="2853b-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="2853b-120">Én eller flere regnskapsdistribusjoner er enten over- eller underdistribuert.</span><span class="sxs-lookup"><span data-stu-id="2853b-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="2853b-121">Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.</span><span class="sxs-lookup"><span data-stu-id="2853b-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="2853b-122">Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**.</span><span class="sxs-lookup"><span data-stu-id="2853b-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="2853b-123">Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="2853b-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="2853b-124">Hvis en leveringsrest blir annullert på en bestilling der endringsstyring er aktivert, går bestillingen til en bekreftet status.</span><span class="sxs-lookup"><span data-stu-id="2853b-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2853b-125">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="2853b-125">Issue description</span></span>

<span data-ttu-id="2853b-126">For en bestilling som er underlagt endringsstyring, hvis den eneste endringen som blir forespurt, er annullering av en leveringsrest på én eller flere av linjene, vil bestillingen gå direkte til en *Bekreftet* tilstand når den er godkjent, og det vil ikke bli opprettet noen journal.</span><span class="sxs-lookup"><span data-stu-id="2853b-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2853b-127">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="2853b-127">Issue resolution</span></span>

<span data-ttu-id="2853b-128">Annullering av en leveringsrest påvirker ikke innholdet i bekreftelsesjournalen.</span><span class="sxs-lookup"><span data-stu-id="2853b-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="2853b-129">Denne funksjonaliteten bør brukes når linjen er delvis mottatt, og den gjenværende kvaliteten skal avbrytes i prosesstrinnet etter at bestillingen er bekreftet hos leverandøren.</span><span class="sxs-lookup"><span data-stu-id="2853b-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="2853b-130">Hvis dette skal reflekteres på bestillingsbekreftelsen, skal antallet justeres på bestillingslinjen slik at bekreftelsen blir nødvendig.</span><span class="sxs-lookup"><span data-stu-id="2853b-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="2853b-131">Hvis det ikke er mottatt noe på linjen, kan du eventuelt fjerne antallet.</span><span class="sxs-lookup"><span data-stu-id="2853b-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="2853b-132">I dette tilfellet kreves det en bekreftelse på nytt.</span><span class="sxs-lookup"><span data-stu-id="2853b-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="2853b-133">Annullerte bestillinger vises i kladdelisten i arbeidsområdet for bestillingsforberedelse.</span><span class="sxs-lookup"><span data-stu-id="2853b-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2853b-134">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="2853b-134">Issue description</span></span>

<span data-ttu-id="2853b-135">Når du har annullert bestillinger som var i *Bekreftet* tilstand, vises de annullerte bestillingene likevel i listen over utkastbestillinger i arbeidsområdet for **Bestillingsklargjøring**.</span><span class="sxs-lookup"><span data-stu-id="2853b-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2853b-136">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="2853b-136">Issue resolution</span></span>

<span data-ttu-id="2853b-137">Dette problemet oppstår bare for bestillinger som er underlagt endringsadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="2853b-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="2853b-138">Dette skjer fordi avlysningen regnes som en endring som må godkjennes.</span><span class="sxs-lookup"><span data-stu-id="2853b-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="2853b-139">Godkjenningen kan gjøres automatisk av systemet.</span><span class="sxs-lookup"><span data-stu-id="2853b-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="2853b-140">Prosessen er derfor å sende den annullerte bestillingen til godkjenningsarbeidsflyten slik at den kan gå til *Godkjent* tilstand.</span><span class="sxs-lookup"><span data-stu-id="2853b-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="2853b-141">På dette punktet vises ikke bestillingen lenger i listen over bestillingsforslag i arbeidsområdet **Bestillingsklargjøring**.</span><span class="sxs-lookup"><span data-stu-id="2853b-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

