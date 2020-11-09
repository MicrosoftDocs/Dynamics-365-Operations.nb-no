---
title: Konsolidere forsendelser når policyen for forsendelseskonsolidering overstyres fra siden Frigi til lager
description: Dette emnet viser et scenario der én eller flere salgslinjer må frigis manuelt til lageret fra siden Frigi til lager, og den systemdefinerte policyen for forsendelseskonsolidering må overstyres før utgivelsen.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 96f994e9f3440721105545f96d7d8475fcab2b6b
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016799"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="88d61-103">Konsolidere forsendelser når policyen for forsendelseskonsolidering overstyres fra siden Frigi til lager</span><span class="sxs-lookup"><span data-stu-id="88d61-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88d61-104">Dette emnet viser et scenario der én eller flere salgslinjer må frigis manuelt til lageret fra siden **Frigi til lager** , og den systemdefinerte policyen for forsendelseskonsolidering må overstyres før utgivelsen.</span><span class="sxs-lookup"><span data-stu-id="88d61-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="88d61-105">Det kan være nødvendig å overstyre en policy for forsendelseskonsolidering hvis en ordre som vanligvis ikke er konsolidert med åpne forsendelser, for eksempel skal konsolideres med åpne forsendelser.</span><span class="sxs-lookup"><span data-stu-id="88d61-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="88d61-106">I løpet av  skal du opprette et sett med salgsordrer og deretter overstyre standardinnstillingen for forsendelseskonsolidering før du frigir ordrene til lageret.</span><span class="sxs-lookup"><span data-stu-id="88d61-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="88d61-107">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="88d61-107">Make demo data available</span></span>

<span data-ttu-id="88d61-108"> i dette emnet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="88d61-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="88d61-109">Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="88d61-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="88d61-110">Definer policyer for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="88d61-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="88d61-111"> som beskrives her, forutsetter at du allerede har aktivert funksjonen, utførte øvelsene i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og opprettet policyer og andre poster som er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="88d61-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="88d61-112">Husk å utføre øvelsene før du fortsetter med dette .</span><span class="sxs-lookup"><span data-stu-id="88d61-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="88d61-113">Opprett salgsordrene for dette </span><span class="sxs-lookup"><span data-stu-id="88d61-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="88d61-114">Gå til **Kunde \> Ordrer \> Alle salgsordrer** , og opprett tre identiske salgsordrer med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="88d61-114">Go to **Accounts receivable \> Orders \> All sales orders** , and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="88d61-115">**Kundekonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="88d61-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="88d61-116">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="88d61-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88d61-117">**Varenummer:** *A0001* (en vare uten **Kode 4** -filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="88d61-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88d61-118">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88d61-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88d61-119">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="88d61-119">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="88d61-120">Frigi salgsordrene fra siden Frigi til lager</span><span class="sxs-lookup"><span data-stu-id="88d61-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="88d61-121">Følg disse trinnene for å overstyre policyen for forsendelseskonsolidering under frigivelse til lageret.</span><span class="sxs-lookup"><span data-stu-id="88d61-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="88d61-122">Gå til **Lagerstyring \> Frigi til lager \> Frigi til lager**.</span><span class="sxs-lookup"><span data-stu-id="88d61-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="88d61-123">I den øvre ruten velger du den første salgsordren du opprettet for dette .</span><span class="sxs-lookup"><span data-stu-id="88d61-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="88d61-124">Velg **Legg til** for å legge til linjen i frigivelsen til lageret.</span><span class="sxs-lookup"><span data-stu-id="88d61-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="88d61-125">Legg merke til at policyen for forsendelseskonsolidering av typen *Standard* brukes i den nederste ruten.</span><span class="sxs-lookup"><span data-stu-id="88d61-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="88d61-126">I den nederste ruten velger du **Velg ny policy for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="88d61-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="88d61-127">Velg en policy som tillater konsolidering med andre åpne forsendelser av samme policy.</span><span class="sxs-lookup"><span data-stu-id="88d61-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="88d61-128">Velg for eksempel policyen *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="88d61-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="88d61-129">Velg **Frigi til lager**.</span><span class="sxs-lookup"><span data-stu-id="88d61-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="88d61-130">Velg den andre og tredje salgsordren du opprettet for dette .</span><span class="sxs-lookup"><span data-stu-id="88d61-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="88d61-131">Velg **Legg til** for å legge til linjene i frigivelsen til lageret.</span><span class="sxs-lookup"><span data-stu-id="88d61-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="88d61-132">Legg merke til at policyen av typen *Standard* brukes i den nederste ruten.</span><span class="sxs-lookup"><span data-stu-id="88d61-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="88d61-133">Velg den andre linjen, og deretter velger du policyen *CustomerOrderNo* i feltet **Velg ny policy for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="88d61-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="88d61-134">Velg **Frigi til lager** for begge linjene.</span><span class="sxs-lookup"><span data-stu-id="88d61-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="88d61-135">Bekrefte forsendelsene</span><span class="sxs-lookup"><span data-stu-id="88d61-135">Verify the shipments</span></span>

<span data-ttu-id="88d61-136">To forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="88d61-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="88d61-137">Den første forsendelsen inneholder to linjer og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="88d61-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="88d61-138">Den andre forsendelsen inneholder én linje og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *Standard*.</span><span class="sxs-lookup"><span data-stu-id="88d61-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="88d61-139">Følg disse trinnene for å se gjennom forsendelsene som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="88d61-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="88d61-140">Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="88d61-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="88d61-141">Finn og velg den påkrevde forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="88d61-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="88d61-142">I feltet **Policy for forsendelseskonsolidering** ser du gjennom konsolideringspolicyen som ble brukt da forsendelsen ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="88d61-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88d61-143">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="88d61-143">Additional resources</span></span>

- [<span data-ttu-id="88d61-144">Policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="88d61-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="88d61-145">Konfigurere policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="88d61-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
