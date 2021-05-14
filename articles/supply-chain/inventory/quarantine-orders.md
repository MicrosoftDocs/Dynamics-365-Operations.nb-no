---
title: Karanteneordrer
description: Dette emnet beskriver hvordan karanteneordrer brukes til å blokkere beholdning.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956188"
---
# <a name="quarantine-orders"></a><span data-ttu-id="9bb1c-103">Karanteneordrer</span><span class="sxs-lookup"><span data-stu-id="9bb1c-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bb1c-104">Dette emnet beskriver hvordan karanteneordrer brukes til å blokkere beholdning.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="9bb1c-105">Du kan bruke karanteneordrer til å blokkere beholdning.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="9bb1c-106">Du kan for eksempel sette varer i karantene av kvalitetskontrollgrunner.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="9bb1c-107">Beholdning som har blitt satt i karantene overføres til et karantenelager.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="9bb1c-108">Hvis du bruker avanserte lagerstyringsprosesser (i Lagerstyring), brukes behandling av karanteneordrer bare for retur av salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="9bb1c-109">Sette lagerbeholdningsvarer i karantene</span><span class="sxs-lookup"><span data-stu-id="9bb1c-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="9bb1c-110">Når du setter varer i karantene, kan du opprette karanteneordrene manuelt eller konfigurere systemet til å opprette dem automatisk under innkommende behandling.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="9bb1c-111">Følg denne fremgangsmåten for å sette opp systemet slik at det automatisk genererer karanteneordrer.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="9bb1c-112">Gå til **Lagerstyring \> Oppsett \> Lager \> Varemodellgrupper**.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="9bb1c-113">Velg en relevant modellgruppe i listeruten, eller opprett en ny modellgruppe.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="9bb1c-114">Merk av for **Overstyr reservering for vareproduksjon** i hurtigfanen **Karantenestyring**.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="9bb1c-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-115">Close the page.</span></span>
1. <span data-ttu-id="9bb1c-116">Angi et standard karantenelager i feltet **Karantenelager** for de mottakende lagrene.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="9bb1c-117">Når en vare som er registrert som mottatt på lageret, tilhører en modellgruppe der det er merket av for **Karantenestyring**, genererer systemet en karanteneordre for den.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="9bb1c-118">Karanteneordren ber arbeiderne om å flytte varen til karantenelageret.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="9bb1c-119">Når du oppretter karanteneordrer manuelt på **Karanteneordrer**-siden, trenger ikke den gjeldende varen være definert for karantenestyring i den tilknyttede varemodellgruppen.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="9bb1c-120">For denne prosessen må du angi lagerbeholdningen som skal være satt i karantene, og karantenelageret som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="9bb1c-121">Du kan bruke karanteneordrestatusene til å planlegge prosessen.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="9bb1c-122">Statuser for karanteneordrer</span><span class="sxs-lookup"><span data-stu-id="9bb1c-122">Quarantine order statuses</span></span>

<span data-ttu-id="9bb1c-123">Karanteneordrer kan ha følgende statuser:</span><span class="sxs-lookup"><span data-stu-id="9bb1c-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="9bb1c-124">Opprettet</span><span class="sxs-lookup"><span data-stu-id="9bb1c-124">Created</span></span>
- <span data-ttu-id="9bb1c-125">Startet</span><span class="sxs-lookup"><span data-stu-id="9bb1c-125">Started</span></span>
- <span data-ttu-id="9bb1c-126">Ferdigmeldt</span><span class="sxs-lookup"><span data-stu-id="9bb1c-126">Reported as finished</span></span>
- <span data-ttu-id="9bb1c-127">Avsluttet</span><span class="sxs-lookup"><span data-stu-id="9bb1c-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="9bb1c-128">Opprettet</span><span class="sxs-lookup"><span data-stu-id="9bb1c-128">Created</span></span>

<span data-ttu-id="9bb1c-129">Når en karanteneordre er opprettet manuelt, men varen ennå ikke er plassert i karantenelageret, har karanteneordren statusen **Opprettet**.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="9bb1c-130">Det genereres to lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="9bb1c-131">Den ene transaksjonen er en avgangstransaksjon som kan ha statusene **I ordre**, **Fysisk reservert** eller **Plukket**.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="9bb1c-132">Den andre transaksjonen er en mottakstransaksjon som kan ha statusene **Bestilt** eller **Registrert** i karantenelageret.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="9bb1c-133">Du kan reservere, plukke og registrere oppdateringer i beholdningen ved hjelp av de vanlige prosessene.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="9bb1c-134">Startet</span><span class="sxs-lookup"><span data-stu-id="9bb1c-134">Started</span></span>

<span data-ttu-id="9bb1c-135">Når en karanteneordre har statusen **Startet**, blir beholdningen overført fra det vanlige lageret til karantenelageret, og to lagertransaksjoner blir generert.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="9bb1c-136">Én transaksjon har statusen **Fratrukket**, og den andre transaksjonen har statusen **Mottatt**.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="9bb1c-137">Samtidig blir to lagertransaksjoner opprettet for å håndtere returoverføringen.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="9bb1c-138">Disse transaksjonene er ikke datert.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-138">These transactions aren't dated.</span></span> <span data-ttu-id="9bb1c-139">Én transaksjon har statusen **Fysisk reservert**, og den andre transaksjonen har statusen **Bestilt**.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="9bb1c-140">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="9bb1c-140">Reported as finished</span></span>

<span data-ttu-id="9bb1c-141">Hvis du vil rapportere en startet karanteneordre som fullført, åpner du ordren og velger **Ferdigmeld** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="9bb1c-142">Varen frigis fra karantenen, men flyttes ikke ennå tilbake til det vanlige lageret.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="9bb1c-143">Flyttingen tilbake til det vanlige lageret kan behandles via en vareankomstjournal som kan startes under ferdigmeldingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="9bb1c-144">Avsluttet</span><span class="sxs-lookup"><span data-stu-id="9bb1c-144">Ended</span></span>

<span data-ttu-id="9bb1c-145">Når en karanteneordre blir ferdig, flyttes varen fra karantenelageret tilbake til det vanlige lageret.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="9bb1c-146">Statusen for varetransaksjonen settes til *Solgt* i karantenelageret og *Kjøpt* i det vanlige lageret.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="9bb1c-147">Karanteneordresvinn</span><span class="sxs-lookup"><span data-stu-id="9bb1c-147">Quarantine order scrap</span></span>

<span data-ttu-id="9bb1c-148">Du kan kassere beholdning som en del av karantenebestillingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="9bb1c-149">Når du behandler svinn, blir statusen for beholdningen angitt til *Solgt* av en avgangstransaksjon fra karantenelageret.</span><span class="sxs-lookup"><span data-stu-id="9bb1c-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bb1c-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9bb1c-150">Additional resources</span></span>

- [<span data-ttu-id="9bb1c-151">Lagerblokkering</span><span class="sxs-lookup"><span data-stu-id="9bb1c-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
