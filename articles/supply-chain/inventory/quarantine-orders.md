---
title: Karanteneordrer
description: Dette emnet beskriver hvordan karanteneordrer brukes til å blokkere beholdning.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14c6f3bae224540968d37de9effa4c430307975c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250871"
---
# <a name="quarantine-orders"></a><span data-ttu-id="4916c-103">Karanteneordrer</span><span class="sxs-lookup"><span data-stu-id="4916c-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4916c-104">Dette emnet beskriver hvordan karanteneordrer brukes til å blokkere beholdning.</span><span class="sxs-lookup"><span data-stu-id="4916c-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="4916c-105">Karanteneordrer kan brukes til å blokkere lager.</span><span class="sxs-lookup"><span data-stu-id="4916c-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="4916c-106">Du kan for eksempel sette varer i karantene av kvalitetskontrollgrunner.</span><span class="sxs-lookup"><span data-stu-id="4916c-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="4916c-107">Beholdning som har blitt satt i karantene overføres til et karantenelager.</span><span class="sxs-lookup"><span data-stu-id="4916c-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="4916c-108">**Obs!** Hvis du bruker avanserte lagerstyringsprosesser (i Lagerstyring), brukes behandling av karanteneordrer bare for retur av salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4916c-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="4916c-109">Sette lagerbeholdningsvarer i karantene</span><span class="sxs-lookup"><span data-stu-id="4916c-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="4916c-110">Når du setter varer i karantene, kan du opprette karanteneordrene manuelt eller konfigurere systemet til å opprette karanteneordrene automatisk under innkommende behandling.</span><span class="sxs-lookup"><span data-stu-id="4916c-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="4916c-111">Du kan opprette karanteneordrer automatisk ved å velge **Karantenestyring** i kategorien **Beholdningspolicyer** på siden **Varemodellgrupper**.</span><span class="sxs-lookup"><span data-stu-id="4916c-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="4916c-112">Du må også angi et standard karantenelager i feltet **Karantenelager** for de mottakende lagrene.</span><span class="sxs-lookup"><span data-stu-id="4916c-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="4916c-113">Når den fysiske lagerbeholdningen er registrert i en bestilling eller produksjonsordre, flyttes varer i karantene automatisk til et karantenelager i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4916c-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Supply Chain Management.</span></span> <span data-ttu-id="4916c-114">Denne bevegelsen oppstår fordi statusen for karanteneordren er endret til **Startet**.</span><span class="sxs-lookup"><span data-stu-id="4916c-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="4916c-115">Når du opprette karanteneordrer manuelt, trenger ikke den gjeldende varen være definert for karantenestyring i den tilknyttede varemodellgruppen.</span><span class="sxs-lookup"><span data-stu-id="4916c-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="4916c-116">For denne prosessen må du angi lagerbeholdningen som skal være satt i karantene, og karantenelageret som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="4916c-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="4916c-117">Du kan bruke karanteneordrestatusene til å planlegge prosessen.</span><span class="sxs-lookup"><span data-stu-id="4916c-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="4916c-118">Statuser for karanteneordrer</span><span class="sxs-lookup"><span data-stu-id="4916c-118">Quarantine order statuses</span></span>
<span data-ttu-id="4916c-119">Karanteneordrer kan ha følgende statuser:</span><span class="sxs-lookup"><span data-stu-id="4916c-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="4916c-120">Opprettet</span><span class="sxs-lookup"><span data-stu-id="4916c-120">Created</span></span>
-   <span data-ttu-id="4916c-121">Startet</span><span class="sxs-lookup"><span data-stu-id="4916c-121">Started</span></span>
-   <span data-ttu-id="4916c-122">Ferdigmeldt</span><span class="sxs-lookup"><span data-stu-id="4916c-122">Reported as finished</span></span>
-   <span data-ttu-id="4916c-123">Avsluttet</span><span class="sxs-lookup"><span data-stu-id="4916c-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="4916c-124">Opprettet</span><span class="sxs-lookup"><span data-stu-id="4916c-124">Created</span></span>

<span data-ttu-id="4916c-125">Når en karanteneordre er opprettet manuelt, men varen ennå ikke er plassert i karantenelageret, har karanteneordren statusen **Opprettet**.</span><span class="sxs-lookup"><span data-stu-id="4916c-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="4916c-126">Det genereres to lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="4916c-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="4916c-127">Den ene transaksjonen er en avgangstransaksjon som kan ha statusene **I ordre**, **Fysisk reservert** eller **Plukket**.</span><span class="sxs-lookup"><span data-stu-id="4916c-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="4916c-128">Den andre transaksjonen er en mottakstransaksjon som kan ha statusene **Bestilt** eller **Registrert** i karantenelageret.</span><span class="sxs-lookup"><span data-stu-id="4916c-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="4916c-129">Du kan reservere, plukke og registrere oppdateringer i beholdningen ved hjelp av de vanlige prosessene.</span><span class="sxs-lookup"><span data-stu-id="4916c-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="4916c-130">Startet</span><span class="sxs-lookup"><span data-stu-id="4916c-130">Started</span></span>

<span data-ttu-id="4916c-131">Når en karanteneordre har statusen **Startet**, blir beholdningen overført fra det vanlige lageret til karantenelageret, og to lagertransaksjoner blir generert.</span><span class="sxs-lookup"><span data-stu-id="4916c-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="4916c-132">Én transaksjon har statusen **Fratrukket**, og den andre transaksjonen har statusen **Mottatt**.</span><span class="sxs-lookup"><span data-stu-id="4916c-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="4916c-133">Samtidig blir to lagertransaksjoner opprettet for å håndtere returoverføringen.</span><span class="sxs-lookup"><span data-stu-id="4916c-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="4916c-134">Disse transaksjonene er ikke datert.</span><span class="sxs-lookup"><span data-stu-id="4916c-134">These transactions aren't dated.</span></span> <span data-ttu-id="4916c-135">Én transaksjon har statusen **Fysisk reservert**, og den andre transaksjonen har statusen **Bestilt**.</span><span class="sxs-lookup"><span data-stu-id="4916c-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="4916c-136">Ferdigmeldt</span><span class="sxs-lookup"><span data-stu-id="4916c-136">Reported as finished</span></span>

<span data-ttu-id="4916c-137">Ved å klikke **Rapporter som fullført** kan du rapportere en startet karanteneordre som fullført.</span><span class="sxs-lookup"><span data-stu-id="4916c-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="4916c-138">Varen frigis fra karantenen, men flyttes ikke ennå tilbake til det vanlige lageret.</span><span class="sxs-lookup"><span data-stu-id="4916c-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="4916c-139">Flyttingen tilbake til det vanlige lageret kan behandles via en vareankomstjournal som kan startes under ferdigmeldingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="4916c-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="4916c-140">Avsluttet</span><span class="sxs-lookup"><span data-stu-id="4916c-140">Ended</span></span>

<span data-ttu-id="4916c-141">Når en karanteneordre blir ferdig, flyttes varen fra karantenelageret tilbake til det vanlige lageret.</span><span class="sxs-lookup"><span data-stu-id="4916c-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="4916c-142">Statusen for varetransaksjonen settes til **Solgt** i karantenelageret og **Kjøpt** i det vanlige lageret.</span><span class="sxs-lookup"><span data-stu-id="4916c-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="4916c-143">Karanteneordresvinn</span><span class="sxs-lookup"><span data-stu-id="4916c-143">Quarantine order scrap</span></span>
<span data-ttu-id="4916c-144">Du kan kassere beholdning som en del av karantenebestillingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="4916c-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="4916c-145">Når du behandler svinn, blir statusen for beholdningen angitt til **Solgt** av en avgangstransaksjon fra karantenelageret.</span><span class="sxs-lookup"><span data-stu-id="4916c-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="additional-resources"></a><span data-ttu-id="4916c-146">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4916c-146">Additional resources</span></span>
--------

[<span data-ttu-id="4916c-147">Lagerblokkering</span><span class="sxs-lookup"><span data-stu-id="4916c-147">Inventory blocking</span></span>](inventory-blocking.md)
