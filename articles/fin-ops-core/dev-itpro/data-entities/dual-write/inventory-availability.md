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
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4455827"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="4f1a7-103">Beholdningstilgjengelighet i dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="4f1a7-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f1a7-104">Ve å bruke beholdningstilgjengelighet kan du kontrollere beholdningen før du legger til et produkt på sidene **Tilbud**, **Ordre** eller **Fakturaer** i Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="4f1a7-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="4f1a7-105">Du kan for eksempel kontrollere beholdning og fastslå en fullføringsdato som én hovedoppgave i [kundeemne-til-kontanter](dual-write-prospect-to-cash.md)-prosessen.</span><span class="sxs-lookup"><span data-stu-id="4f1a7-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="4f1a7-106">Hvis du ikke har nok beholdning, kan du beregne en leveringsdato basert på prosjekterte beholdningsmottak og -problemer.</span><span class="sxs-lookup"><span data-stu-id="4f1a7-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="4f1a7-107">Du kan også kontrollere produktets tilgjengelig for ordre (ATP)-informasjon, der du kan finne ATP-antallet i den forhåndsdefinerte tidshorisonten.</span><span class="sxs-lookup"><span data-stu-id="4f1a7-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="4f1a7-108">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="4f1a7-108">On-hand inventory</span></span>

<span data-ttu-id="4f1a7-109">I Dynamics 365 Sales er en ny **Lagerbeholdning**-knapp lagt til i hodet på sidene **Tilbud**, **Ordrer** og **Fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="4f1a7-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="4f1a7-110">Når du velger denne knappen, vises det en dialogboks hvor du kan angi firmaet og produktet du vil kontrollere tilgjengelig beholdning for.</span><span class="sxs-lookup"><span data-stu-id="4f1a7-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="4f1a7-111">Denne dialogboksen viser den samme informasjonen som [Lagerbeholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="4f1a7-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="4f1a7-112">Dialogboksen returnerer lagerinformasjonen fra Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4f1a7-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4f1a7-113">Denne informasjonen inneholder følgende antall:</span><span class="sxs-lookup"><span data-stu-id="4f1a7-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="4f1a7-114">Antall på lager</span><span class="sxs-lookup"><span data-stu-id="4f1a7-114">On-hand quantity</span></span>
- <span data-ttu-id="4f1a7-115">Antall reservert på lager</span><span class="sxs-lookup"><span data-stu-id="4f1a7-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="4f1a7-116">Antall tilgjengelig på lager</span><span class="sxs-lookup"><span data-stu-id="4f1a7-116">Available on-hand quantity</span></span>
- <span data-ttu-id="4f1a7-117">Bestilt antall</span><span class="sxs-lookup"><span data-stu-id="4f1a7-117">Ordered quantity</span></span>
- <span data-ttu-id="4f1a7-118">Antall i bestilling</span><span class="sxs-lookup"><span data-stu-id="4f1a7-118">On-order quantity</span></span>
- <span data-ttu-id="4f1a7-119">Reservert bestilt antall</span><span class="sxs-lookup"><span data-stu-id="4f1a7-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="4f1a7-120">Totalt tilgjengelig antall</span><span class="sxs-lookup"><span data-stu-id="4f1a7-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="4f1a7-121">ATP-informasjon</span><span class="sxs-lookup"><span data-stu-id="4f1a7-121">ATP information</span></span>

<span data-ttu-id="4f1a7-122">I Sales er det lagt til en ny **ATP-informasjon**-knapp for linjeelementer på sidene **Tilbud**, **Ordrer** og **Fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="4f1a7-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="4f1a7-123">Når du velger denne knappen, vises det en dialogboks hvor du kan angi firma, produkt, beholdningsnettsted, beholdningslager og ordreantall.</span><span class="sxs-lookup"><span data-stu-id="4f1a7-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="4f1a7-124">Denne dialogboksen har de samme innstillingene som er beskrevet i [Ordrebekreftelse](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="4f1a7-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="4f1a7-125">Dialogboksen returnerer ATP-informasjonen fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4f1a7-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="4f1a7-126">Denne informasjonen inneholder følgende antall:</span><span class="sxs-lookup"><span data-stu-id="4f1a7-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="4f1a7-127">ATP-antall</span><span class="sxs-lookup"><span data-stu-id="4f1a7-127">ATP quantity</span></span>
- <span data-ttu-id="4f1a7-128">Tilgangsantall</span><span class="sxs-lookup"><span data-stu-id="4f1a7-128">Receipt quantity</span></span>
- <span data-ttu-id="4f1a7-129">Avgangsantall</span><span class="sxs-lookup"><span data-stu-id="4f1a7-129">Issue quantity</span></span>
- <span data-ttu-id="4f1a7-130">Antall på lager</span><span class="sxs-lookup"><span data-stu-id="4f1a7-130">On-hand quantity</span></span>
