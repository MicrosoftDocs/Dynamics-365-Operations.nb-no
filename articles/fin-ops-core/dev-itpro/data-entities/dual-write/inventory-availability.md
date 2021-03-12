---
title: Beholdningstilgjengelighet i dobbel skriving
description: Dette emnet inneholder informasjon om hvordan beholdningstilgjengelighet i dobbel skriving sjekkes.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839555"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="e88ee-103">Beholdningstilgjengelighet i dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="e88ee-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e88ee-104">Ve å bruke beholdningstilgjengelighet kan du kontrollere beholdningen før du legger til et produkt på sidene **Tilbud**, **Ordre** eller **Fakturaer** i Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e88ee-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="e88ee-105">Du kan for eksempel kontrollere beholdning og fastslå en fullføringsdato som én hovedoppgave i [kundeemne-til-kontanter](dual-write-prospect-to-cash.md)-prosessen.</span><span class="sxs-lookup"><span data-stu-id="e88ee-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="e88ee-106">Hvis du ikke har nok beholdning, kan du beregne en leveringsdato basert på prosjekterte beholdningsmottak og -problemer.</span><span class="sxs-lookup"><span data-stu-id="e88ee-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="e88ee-107">Du kan også kontrollere produktets tilgjengelig for ordre (ATP)-informasjon, der du kan finne ATP-antallet i den forhåndsdefinerte tidshorisonten.</span><span class="sxs-lookup"><span data-stu-id="e88ee-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="e88ee-108">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="e88ee-108">On-hand inventory</span></span>

<span data-ttu-id="e88ee-109">I Dynamics 365 Sales er en ny **Lagerbeholdning**-knapp lagt til i hodet på sidene **Tilbud**, **Ordrer** og **Fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="e88ee-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="e88ee-110">Når du velger denne knappen, vises det en dialogboks hvor du kan angi firmaet og produktet du vil kontrollere tilgjengelig beholdning for.</span><span class="sxs-lookup"><span data-stu-id="e88ee-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="e88ee-111">Denne dialogboksen viser den samme informasjonen som [Lagerbeholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="e88ee-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="e88ee-112">Dialogboksen returnerer lagerinformasjonen fra Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e88ee-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e88ee-113">Denne informasjonen inneholder følgende antall:</span><span class="sxs-lookup"><span data-stu-id="e88ee-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="e88ee-114">Antall på lager</span><span class="sxs-lookup"><span data-stu-id="e88ee-114">On-hand quantity</span></span>
- <span data-ttu-id="e88ee-115">Antall reservert på lager</span><span class="sxs-lookup"><span data-stu-id="e88ee-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="e88ee-116">Antall tilgjengelig på lager</span><span class="sxs-lookup"><span data-stu-id="e88ee-116">Available on-hand quantity</span></span>
- <span data-ttu-id="e88ee-117">Bestilt antall</span><span class="sxs-lookup"><span data-stu-id="e88ee-117">Ordered quantity</span></span>
- <span data-ttu-id="e88ee-118">Antall i bestilling</span><span class="sxs-lookup"><span data-stu-id="e88ee-118">On-order quantity</span></span>
- <span data-ttu-id="e88ee-119">Reservert bestilt antall</span><span class="sxs-lookup"><span data-stu-id="e88ee-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="e88ee-120">Totalt tilgjengelig antall</span><span class="sxs-lookup"><span data-stu-id="e88ee-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="e88ee-121">ATP-informasjon</span><span class="sxs-lookup"><span data-stu-id="e88ee-121">ATP information</span></span>

<span data-ttu-id="e88ee-122">I Sales er det lagt til en ny **ATP-informasjon**-knapp for linjeelementer på sidene **Tilbud**, **Ordrer** og **Fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="e88ee-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="e88ee-123">Når du velger denne knappen, vises det en dialogboks hvor du kan angi firma, produkt, beholdningsnettsted, beholdningslager og ordreantall.</span><span class="sxs-lookup"><span data-stu-id="e88ee-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="e88ee-124">Denne dialogboksen har de samme innstillingene som er beskrevet i [Ordrebekreftelse](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="e88ee-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="e88ee-125">Dialogboksen returnerer ATP-informasjonen fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e88ee-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="e88ee-126">Denne informasjonen inneholder følgende antall:</span><span class="sxs-lookup"><span data-stu-id="e88ee-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="e88ee-127">ATP-antall</span><span class="sxs-lookup"><span data-stu-id="e88ee-127">ATP quantity</span></span>
- <span data-ttu-id="e88ee-128">Tilgangsantall</span><span class="sxs-lookup"><span data-stu-id="e88ee-128">Receipt quantity</span></span>
- <span data-ttu-id="e88ee-129">Avgangsantall</span><span class="sxs-lookup"><span data-stu-id="e88ee-129">Issue quantity</span></span>
- <span data-ttu-id="e88ee-130">Antall på lager</span><span class="sxs-lookup"><span data-stu-id="e88ee-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="e88ee-131">Hvordan det fungerer</span><span class="sxs-lookup"><span data-stu-id="e88ee-131">How it works</span></span>

<span data-ttu-id="e88ee-132">Når du velger knappen **Lagerbeholdning** på siden **Tilbud**, **Ordrer** eller **Fakturaer**, foretas et live oppkall med dobbel skriving til API-en for **Lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="e88ee-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="e88ee-133">API-en beregner lagerbeholdningen for det angitte produktet.</span><span class="sxs-lookup"><span data-stu-id="e88ee-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="e88ee-134">Resultatet blir lagret i tabellene **InventCDSInventoryOnHandRequestEntity** og **InventCDSInventoryOnHandEntryEntity** og skrives deretter til Dataverse av dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="e88ee-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="e88ee-135">Hvis du vil bruke denne funksjonaliteten, må du kjøre følgende dobbel skriving-tilordninger.</span><span class="sxs-lookup"><span data-stu-id="e88ee-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="e88ee-136">Hopp over innledende synkronisering når du kjører tilordningene.</span><span class="sxs-lookup"><span data-stu-id="e88ee-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="e88ee-137">Oppføringer for CDS-lagerbeholdning (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="e88ee-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="e88ee-138">Forespørsler om CDS-lagerbeholdning (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="e88ee-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="e88ee-139">Maler</span><span class="sxs-lookup"><span data-stu-id="e88ee-139">Templates</span></span>
<span data-ttu-id="e88ee-140">Følgende maler er tilgjengelige for visning av lagerbeholdningsdata.</span><span class="sxs-lookup"><span data-stu-id="e88ee-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="e88ee-141">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="e88ee-141">Finance and Operations apps</span></span> | <span data-ttu-id="e88ee-142">Kundeengasjementsapp</span><span class="sxs-lookup"><span data-stu-id="e88ee-142">Customer engagement app</span></span> | <span data-ttu-id="e88ee-143">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e88ee-143">Description</span></span> 
---|---|---
[<span data-ttu-id="e88ee-144">Lagerbeholdningsoppføringer for CDS</span><span class="sxs-lookup"><span data-stu-id="e88ee-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="e88ee-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="e88ee-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="e88ee-146">Forespørsler om lagerbeholdning for CDS</span><span class="sxs-lookup"><span data-stu-id="e88ee-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="e88ee-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="e88ee-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="e88ee-148">Oppføringer for CDS-lagerbeholdning (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="e88ee-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="e88ee-149">Denne malen synkroniserer data mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e88ee-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="e88ee-150">Finance and Operations-felt</span><span class="sxs-lookup"><span data-stu-id="e88ee-150">Finance and Operations field</span></span> | <span data-ttu-id="e88ee-151">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="e88ee-151">Map type</span></span> | <span data-ttu-id="e88ee-152">Kundeengasjement-felt</span><span class="sxs-lookup"><span data-stu-id="e88ee-152">Customer engagement field</span></span> | <span data-ttu-id="e88ee-153">Standardverdi</span><span class="sxs-lookup"><span data-stu-id="e88ee-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="e88ee-154">Forespørsler om CDS-lagerbeholdning (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="e88ee-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="e88ee-155">Denne malen synkroniserer data mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e88ee-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="e88ee-156">Finance and Operations-felt</span><span class="sxs-lookup"><span data-stu-id="e88ee-156">Finance and Operations field</span></span> | <span data-ttu-id="e88ee-157">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="e88ee-157">Map type</span></span> | <span data-ttu-id="e88ee-158">Kundeengasjement-felt</span><span class="sxs-lookup"><span data-stu-id="e88ee-158">Customer engagement field</span></span> | <span data-ttu-id="e88ee-159">Standardverdi</span><span class="sxs-lookup"><span data-stu-id="e88ee-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |




